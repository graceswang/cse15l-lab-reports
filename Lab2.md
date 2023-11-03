# Part 1:
### Here is the code for my StringServer:

```ruby
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    StringBuilder print = new StringBuilder();
    int counter = 0;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                counter++;
                print.append(counter+". "+parameters[1]+"\n");
                return String.format(print.toString() +"\n");
            }
        }
        return "404 Not Found!";
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

![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/5743d7d8-15ad-4663-bbf2-d88d2f04b7ae)
- For this screenshot, the port here is 6066, and directs the request to the Handler class. The method handleRequest(URI url) in the Handler class gets called.
- For this method handleRequest(URI url), the relevant argument is the url（http://localhost:6066/add-message?s=Hello). The field here is **print**. Before the request, its value is empty, which is a empty StringBuilder. After the request, its value is the content after **=** that we are trying to append to.
- So here, since the path equals to **/add-message**, the value **"Hello"** is appended to the **print** StringBuilder, the variable **counter** will become **1** as it increments. After this specific request, the **print** StringBuildr will have the value **"1. Hello\n"**. 

![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/cbebe944-05b6-46d0-8f01-c20cc7e5e780)
- For this screenshot, the port here is 6066, and directs the request to the Handler class. The method handleRequest(URI url) in the Handler class gets called.
- For this method handleRequest(URI url), the relevant argument is the url（http://localhost:6066/add-message?s=How are you). The field here is **print**. Before the request, its value is **"Hello\n"**. After the request, its value is the content after **=** that we are trying to append to.
- So here, since the path equals to **/add-message**, the value **"How are you"** is appended to the existing **print** StringBuilder, the variable **counter** will become **2** as it increments once. After this specific request, the **print** StringBuildr which had the value **"1. Hello\n"** from the previous request will now become **"2. Hello\n How are you\n"**.


# Part 2:
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/14351670-f221-42a1-99a5-189b36b9df82)
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/f34ffff9-09b5-42d1-9af6-61459a9cca90)
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/384d1638-8fdb-4e12-b36b-339b878bb6d9)
To show the path to the private key and public key for my SSH key for logging into ieng6, I used ```ls /Users/gracewang/.ssh/id_rsa``` and ```scp /Users/gracewang/.ssh/id_rsa.pub cs15lfa23bo@ieng6.ucsd.edu:~/.ssh/authorized_keys```, and the path for private key is **/Users/gracewang/.ssh/id_rsa** and the path for public key is **/Users/gracewang/.ssh/authorized_keys/id_rsa.pub** which is matched with the saved path in second screenshot. 
A terminal interaction where you log into ieng6 with your course-specific account without being asked for a password:
![image](https://github.com/graceswang/cse15l-lab-reports/assets/135576306/5c164b2f-4160-4d99-b7a9-f3111800cc48)

# Part 3:
I didn't know that how to log in ssh and control the remote computer. I've also never known that we could not only access to the website by adding the url line but also using ``url`` in command line. It is also new for me to log in my ssh account without a password and I think it's good for me, because sometimes I'll forget my password and have to change it. 


  
