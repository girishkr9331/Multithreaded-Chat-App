# MULTITHREADED CHAT APPLICATION

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : GIRISH KUMAR

*INTERN_ID* : CT06DF2915

*DOMAIN* : Java Programming

*DURATION* : 6 WEEKS

*MENTOR* : Neela Santhosh Kumar
  
  
<br/><br/><br/>

## Description

Architecture

* Client-Server Model: Central server coordinates communication between multiple clients  
* Socket Programming: Uses Java ServerSocket (server) and Socket (client) for network communication  
* Port Configuration: Server listens on port 8080 for incoming connections  

Multithreading Implementation

* Server Threading: Each client connection handled by separate ClientHandler thread  
* Client Threading: Main thread for input, MessageListener thread for receiving messages  
* Concurrent Operations: Multiple clients can send/receive messages simultaneously  
* Thread Safety: Synchronized methods prevent race conditions on shared resources  

Core Components
  ChatServer.java  

  * Creates ServerSocket and accepts client connections  
  * Maintains ArrayList of active ClientHandler objects  
  * Broadcasts messages to all connected clients  
  * Manages client connections and disconnections  
  
  ChatClient.java  

  * Connects to server using Socket  
  * Handles user input and message sending  
  * Listens for incoming messages in separate thread  
  * Provides simple command interface (/quit to exit)  

  ClientHandler.java (Inner Class)  

  * Implements Runnable for thread execution  
  * Manages individual client communication  
  * Handles username assignment and message formatting  
  * Performs cleanup on client disconnection  

Key Features  

* Real-time Messaging: Instant message broadcasting to all clients  
* User Management: Username assignment and join/leave notifications  
* Multiple Clients: Supports unlimited simultaneous connections  
* Graceful Disconnection: Proper cleanup and notification when clients leave  
* Error Handling: Network exception management and connection recovery  

Technical Implementation  

* I/O Streams: BufferedReader and PrintWriter for text communication  
* Resource Management: Proper cleanup of sockets and streams  
* Exception Handling: IOException management for network operations  
* Iterator Pattern: Safe client list modification during broadcasting  
* Synchronization: Thread-safe access to shared client list  
 
Programming Concepts Demonstrated  

* Network Programming: TCP socket communication fundamentals  
* Concurrent Programming: Multi-threaded application design  
* Client-Server Architecture: Distributed system communication patterns   
* Resource Management: Proper handling of system resources  

### How It Works  

* Server Startup: ChatServer creates ServerSocket and waits for connections  
* Client Connection: Each client connects via Socket, server creates ClientHandler thread  
* Username Setup: Client provides username, server welcomes and notifies others  
* Message Flow: Client sends message → Server receives → Broadcasts to all other clients  
* Real-time Communication: All clients see messages instantly via dedicated listener threads  
* Disconnection: Client types /quit or closes, server notifies remaining clients  

<br/> <br/>

### Output Images

![](https://github.com/girishkr9331/Multithreaded-Chat-App/blob/main/MultithreadingChat1.png)
![](https://github.com/girishkr9331/Multithreaded-Chat-App/blob/main/MultithreadingChat2.png)
![](https://github.com/girishkr9331/Multithreaded-Chat-App/blob/main/MultithreadingChat3.png)

Chat app using sockets

Instructions :
1. Navigate to the file directory.
2. Run in terminal :  
  javac ServerSide.java ChatClient.java  
  java ServerSide
3. Go to another terminal/ or start a new terminal.
  then, 
  java ChatClient
4. Enter name of the client
5. Join more clients thourgh multiple terminal and chat 
    

