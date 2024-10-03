# Online Chatting Application

This Online Chatting Application allows real-time communication between users. You can use it to chat with your family, friends, or other people. The application is built using Java concepts such as **Swing** for the graphical user interface (GUI) and **Socket Programming** for communication between clients and the server. The project consists of two parts: a **Client-side** and a **Server-side** to manage the communication between users.

## Features

- **Real-Time Chat**: Communicate instantly with others in the application.
- **User Interface**: A simple and clean UI using Java Swing components.
- **Message Display**: Sent and received messages are displayed in the chat window with a timestamp.
- **One-to-One Chat**: The server can manage one-to-one chat sessions between clients.
- **Active Status**: Shows the active status of users.
- **Exit**: Ability to exit the application using a back button.
- **Socket Programming**: Communication is handled using TCP/IP sockets between client and server.

## Tech Stack

- **Java Swing**: For the graphical user interface (UI) components.
- **Socket Programming**: For communication between the client and server.
- **Multithreading**: For handling multiple clients efficiently (extendable for further features).
- **Java I/O Streams**: For input and output operations between the server and client.

## How It Works

### Client-Side (Client.java)
- The client application allows users to send messages to the server and receive responses in real-time.
- The user interface is built using Java Swing and includes elements like chat messages, send button, text field for input, and a profile section.
- The client connects to the server through a socket using `127.0.0.1` (localhost) and port `6001`.

### Server-Side
- The server listens for incoming connections from clients.
- It facilitates the communication between multiple clients by receiving and forwarding messages.
- Once a client sends a message, it is broadcasted to all connected clients.
- The server handles input/output using **DataInputStream** and **DataOutputStream**.

### Communication Flow
1. The client sends a message via the socket connection to the server.
2. The server receives the message and forwards it to the recipient(s).
3. The messages are displayed in the chat window of both the sender and receiver with a timestamp.

## How to Run

1. **Server Side**:
    - Run the server code on your machine.
    - The server will listen for incoming connections on port `6001`.

2. **Client Side**:
    - Run the client code on your machine or another machine.
    - The client connects to the server using the `localhost` IP (`127.0.0.1`) and port `6001`.

3. You can open multiple clients to simulate real-time chatting between different users.

## Code Structure

- **Client.java**: This file contains the client-side code.
  - UI components (chat window, input text field, send button).
  - Socket programming to handle message sending and receiving.
  
- **Server.java**: The server-side code responsible for handling multiple clients.

## Prerequisites

- Java Development Kit (JDK) 8 or higher.
- Basic understanding of Java, Swing, and socket programming.

## How to Compile and Run

1. **Compile the Code**:
    ```bash
    javac Client.java
    javac Server.java
    ```

2. **Run the Server**:
    ```bash
    java Server
    ```

3. **Run the Client**:
    ```bash
    java Client
    ```

4. Open multiple clients to start chatting!

## Future Enhancements

- **Group Chat**: Implement group chat functionality.
- **User Authentication**: Add login and registration features.
- **File Sharing**: Support for sharing files during chat sessions.
- **Enhanced UI**: Improve the user interface for a better user experience.

## Screenshots
_Include screenshots of the chat window, message input, and active user status._

## License
This project is licensed under the MIT License.
