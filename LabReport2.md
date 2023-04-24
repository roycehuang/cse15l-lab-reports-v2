# Lab Report 1 - Remote Access and FileSystem (Week 1)
due Monday, April 24 by 11:59pm

### Part 1 - String Server
``` 
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
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

<img width="482" alt="image" src="https://user-images.githubusercontent.com/130111798/233875530-4dba40a8-e703-4c23-bf81-69e1d8bed10c.png">
