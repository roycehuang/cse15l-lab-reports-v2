# Lab Report 2 - Servers and Bugs (Week 3)
due Monday, April 24 by 11:59pm

### Part 1 - String Server
``` 
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String str = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("%s", str);
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    str += parameters[1] + "\n";
                    return String.format(str);
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

<img width="412" alt="image" src="https://user-images.githubusercontent.com/130111798/233875539-f57c2294-cfa9-4afa-912e-037aa9ae773d.png">

The methods that are called are in the Handler class are the HandleRequest and the relevant arguments are the url which the code parses the path to find a message to add. The values that were changed were str in order to update with the previous string argument. The ```str``` variable changed from an empty string to "Hello".

<img width="482" alt="image" src="https://user-images.githubusercontent.com/130111798/233875530-4dba40a8-e703-4c23-bf81-69e1d8bed10c.png">

The same values changed, with ```str``` changing from "Hello" to "Hello /n hello world".

### Part 2 - Fixing Bugs
The bug that I chose was in the method reverseInPlace. 

A failure-inducing input for the buggy program was..
```
   int[] input2 = { 1, 2 };
   ArrayExamples.reverseInPlace(input2);
   assertArrayEquals(new int[]{2,1}, input2);
```
An input that doesn't induce a failure was..
```
   int[] input2 = { 3 };
   ArrayExamples.reverseInPlace(input2);
   assertArrayEquals(new int[]{3}, input2);
```
<img width="412" alt="image" src="https://user-images.githubusercontent.com/130111798/234188579-8f74d89d-fb24-450e-89ac-ea7c30f2820f.png">

<img width="883" alt="image" src="https://user-images.githubusercontent.com/130111798/234188650-663104ed-d04a-4552-82a2-39a0342dac9f.png">

The original code was: 

```
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
 
```
 
The fixed code was:

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
  ```

The fix addresses the issue, because the code originally was that it would reverse the array list, but then would turn the other half of the list back into not being in order. My fix was to have the for loop only go through the length divided by 2 in integer division so that it wouldn't update already updated values, and added a temporary variable so that the code would update both sides of the array list at once only needing half the iterations.

### Part 3 - Reflection
Something I learned that I didn't know before, was how servers were made. It was interesting how the data from variables are saved so that the data can be updated without deleting previous information.
