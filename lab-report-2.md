# Lab Report 2 - Servers and SSH Keys

Code for ```StringServer``` and ```Server```
![Image](lab2-stringserver-code-1.png)
![Image](lab2-server-code-1.png)

I used the Server file provided from the previous lab assignment.

#Example Calls
![Image](lab2-example1-1.png)

![Image](lab2-example2-1.png)

Which methods in your code are called?
For both examples, we start off by running the main method of the ```StringServer``` class, starting a server with port 4000 in my specific case, as the input String[] args will just be an array with a singular String ```4000```, and ```int port = Integer.parseInt("4000")```.

What are the relevant arguments to those methods, and the values of any relevant fields of the class?
Example 1:
- The first method call is the start method of class Server, which creates a HttpServer object with socket at port 4000, and uses the Handler class in ```StringServer```.
```Server.start(4000, new Handler())```

- The HttpServer object, called server, calls a ```createContext``` method which allows it to take input, specifying paths using a forward slash character, and creates a ServerHttpHandler objects using the rules specified in the ```StringServer``` ```Handler``` class.
```Server.start(4000, new Handler())```

- Example 2:


How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
