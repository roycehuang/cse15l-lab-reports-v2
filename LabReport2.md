# Lab Report 1 - Remote Access and FileSystem (Week 1)
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
Provide:

A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
Briefly describe why the fix addresses the issue.

