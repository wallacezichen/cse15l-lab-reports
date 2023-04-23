# Part1
Here is the code for my StringServer:
![image1](assets/lab2/image1.png)
Here is the screenshots of using `add-message`
![image2](assets/lab2/image2.png)
![image3](assets/lab2/image3.png)
* `Main` method, `Server.start` method, and `handleRequest` method in Handler class are called.
* Essentially I am called the main method in StringServer class. I pass in 4000 as the local host server number this argument is used for port for later method. In the main method, I passed in a new `SearchEngine` object and `port`(a integer(input argument of main method)) as  input for Server object `start` method. Inside the Server.start method, `server.createContext` is called and it takes a String `path` and URLHandler Object `handler` as arguments.
* In my `handleRequest` method, `this.lst` will change everything when the new request has correct query. `this.lst` is a ArrayList that store all of the queries that requested before. And everytime we called the function, it will return them as a String that seperated in different lines.

# Part2

# Part3
