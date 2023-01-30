#CSE15L Lab Report 2

##Part one
Here is the code of StringServer.java:
> import java.io.IOException;
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

