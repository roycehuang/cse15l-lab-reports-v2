# Lab Report 5
due date: Monday June 5, 2023

## Student EdStem Debugging Question
### What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?

MacOS, using VScode

### Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.

From running the test file, this was what the terminal output was. The results from my code differs from that of the tester file.

JUnit version 4.13.2 .E.E Time: 0.022 There were 2 failures:

testMerge1(ListExamplesTests) arrays first differed at element [2]; expected:<[x]> but was:<[a]> at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78) at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28) at org.junit.Assert.internalArrayEquals(Assert.java:534) at org.junit.Assert.assertArrayEquals(Assert.java:285) at org.junit.Assert.assertArrayEquals(Assert.java:300) at ListExamplesTests.testMerge1(ListExamplesTests.java:12) ... 9 trimmed Caused by: org.junit.ComparisonFailure: expected:<[x]> but was:<[a]> at org.junit.Assert.assertEquals(Assert.java:117) at org.junit.Assert.assertEquals(Assert.java:146) at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8) at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76) ... 15 more

testMerge2(ListExamplesTests) arrays first differed at element [4]; expected:<[d]> but was:<[b]> at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78) at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28) at org.junit.Assert.internalArrayEquals(Assert.java:534) at org.junit.Assert.assertArrayEquals(Assert.java:285) at org.junit.Assert.assertArrayEquals(Assert.java:300) at ListExamplesTests.testMerge2(ListExamplesTests.java:19) ... 9 trimmed Caused by: org.junit.ComparisonFailure: expected:<[d]> but was:<[b]> at org.junit.Assert.assertEquals(Assert.java:117) at org.junit.Assert.assertEquals(Assert.java:146) at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8) at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76) ... 15 more

FAILURES!!! Tests run: 2, Failures: 2

### Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.

The failure-inducing input was from attempting to merge {"a","b"}+{"x","y"} and {"a","b","c"}+{"c","d","e"} from both test cases. The last command that I ran was bash test.sh which produced this error as well. I'm not sure why there is an error with the expected "x" and actual "a" when it passed for the first {"a","b"} list. 

## TA Response
Hi Royce! You're on the right track, from what you know of the expected values and the resulting ones, do you think the next elements in the two lists would be the same as well? If not, what would they be and what would that say about your code?

## Student terminal output
JUnit version 4.13.2

..

Time: 0.02


OK (2 tests)

## File/Directory Structure and File contents
lab7/

|- ListExamples.java

|- ListExamplesTests.java

|- test.sh

|- lib/

   > |- hamcrest-core-1.3.jar

   > |- junit-4.13.2.jar
 
 
#### ListExamples.java
```import java.util.ArrayList;
import java.util.List;

interface StringChecker { boolean checkString(String s); }

class ListExamples {

  // Returns a new list that has all the elements of the input list for which
  // the StringChecker returns true, and not the elements that return false, in
  // the same order they appeared in the input list;
  static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for(String s: list) {
      if(sc.checkString(s)) {
        result.add(0, s);
      }
    }
    return result;
  }


  // Takes two sorted list of strings (so "a" appears before "b" and so on),
  // and return a new list that has all the strings in both list in sorted order.
  static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
        result.add(list1.get(index1));
        index1 += 1;
      }
      else {
        result.add(list2.get(index2));
        index2 += 1;
      }
    }
    while(index1 < list1.size()) {
      result.add(list2.get(index1));
      index1 += 1;
    }
    while(index2 < list2.size()) {
      result.add(list1.get(index2));
      // change index1 below to index2 to fix test
      index2 += 1;
    }
    return result;
  }


}
```
                                
#### ListExamplesTests.java
```import static org.junit.Assert.*;
import org.junit.*;
import java.util.*;
import java.util.ArrayList;


public class ListExamplesTests {
        
        @Test(timeout = 500)
        public void testMerge1() {
                List<String> l1 = new ArrayList<String>(Arrays.asList("x", "y"));
                List<String> l2 = new ArrayList<String>(Arrays.asList("a", "b"));
                assertArrayEquals(new String[]{ "a", "b", "x", "y"}, ListExamples.merge(l1, l2).toArray());
        }

        @Test(timeout = 500)
        public void testMerge2() {
                List<String> l1 = new ArrayList<String>(Arrays.asList("a", "b", "c"));
                List<String> l2 = new ArrayList<String>(Arrays.asList("c", "d", "e"));
                assertArrayEquals(new String[]{ "a", "b", "c", "c", "d", "e" }, ListExamples.merge(l1, l2).toArray());
        }

}
```
#### test.sh
```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
### Full Command Line to Trigger the Bug:
```bash test.sh```

### To Fix the Bug:
In order to fix the bug the list1 and list2 need to be switched from the line ```result.add(list2.get(index1));``` to the code ```result.add(list1.get(index1));``` and in the same way for the line ```result.add(list1.get(index2));``` should be changed to ```result.add(list2.get(index2));``` 

## Reflection:
Something that I learned from my lab experience in the second half of this quarter that I didn't know before was how the backend of websites that we use on the daily are coded. I was especially interested in how we were able to mimick Autograder in how it uses bash to efficiently test the code of numerous students at once.
