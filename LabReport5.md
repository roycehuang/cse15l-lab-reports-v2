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



