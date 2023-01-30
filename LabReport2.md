# CSE15L Lab Report 2

## Part one
Here is the code of StringServer.java:
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler{
    String curString = "";
    
    @Override
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) 
            return String.format(curString);
        else if(url.getPath().contains("/add-message"))
        {
            String[] parameters = url.getQuery().split("=");
            if(curString != "")
                curString += "\n";
            if (parameters[0].equals("s"))
                curString += parameters[1];
            return String.format(curString);
        }
        return "404 Not Found!";
    }
}

class StringServer{
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
Scrrenshot 1:\
<img width="432" alt="image" src="https://user-images.githubusercontent.com/122579697/215367311-3d9ac038-e8e3-47a1-9a8b-26422490775c.png">
the url is: "http://localhost:4000/add-message?s=Hello"
* `start(port, new Handler())` is called in the main of StringServer
    * `handleRequest(URI url)` is then called, right now, curString is still "" (an empty string).
        *  `url.getPath().contains("/add-message")` is true so the following are called
            *  `String[] parameters = url.getQuery().split("=");` splits the url into half (s and the string in this case)
            *  `parameters[0].equals("s")` is true because parameters[0] = s in this case, so the following is called 
                *  `curString += parameters[1];` this concatenate the original string with the new string after "s=". parameters[1] = "Hello" in this case.
            *  `return String.format(curString);` and then we return the updated string: "Hello".

Scrrenshot 2:\
<img width="436" alt="image" src="https://user-images.githubusercontent.com/122579697/215367353-b7b50c66-f8d4-479a-8905-f3c31bd26aa4.png">
the url is: "http://localhost:4000/add-message?s=How%20are%20you"
* `start(port, new Handler())` is called in the main of StringServer
    * `handleRequest(URI url)` is then called, curString is still "Hello".
        *  `url.getPath().contains("/add-message")` is true so the following are called
            *  `curString != ""` is true because curString is now "Hello", so the following is called
                *  `curString += "\n";` now a new line char is concatenated to curString
            *  `String[] parameters = url.getQuery().split("=");` splits the url into half (s and the string in this case)
            *  `parameters[0].equals("s")` is true because parameters[0] = s in this case, so the following is called 
                *  `curString += parameters[1];` this concatenate the original string with the new string after "s=". parameters[1] = "How are you" in this case.
            *  `return String.format(curString);` and then we return the updated string: "Hello\nHow are you".

## Part 2
