# Chatting Application

## Overview

This project is a simple chat application implemented in Java using `Swing` for the GUI, and `Socket` programming for client-server communication. It enables two users (client and server) to send and receive text messages in real time.

## Features

1. **Graphical User Interface (GUI)**:
   - Each user (client and server) has a visually appealing window.
   - The chat interface includes icons for video call, audio call, and more options (currently placeholders with no functionality).
   - Real-time text message display between two users.
   - Displays sender's name and active status (e.g., "Active Now").
   - Scrollable chat history in both client and server windows.

2. **Client-Server Communication**:
   - Uses `Socket` programming for communication between the client and server.
   - Messages are sent as UTF-encoded strings using `DataInputStream` and `DataOutputStream`.
   - The server listens on a specified port for incoming client connections.

## Project Structure

### Client Class (`Client.java`)

- Implements the client-side of the chat application.
- **Components**:
  - `JTextField`: For message input by the client.
  - `JPanel`: For displaying sent and received messages.
  - `DataOutputStream`: To send messages to the server.
- **Key Functions**:
  - `actionPerformed()`: Sends the text message when the "Send" button is clicked.
  - `formatLabel()`: Formats the outgoing message in a visually appealing format with a timestamp.
  - `main()`: Establishes a socket connection to the server and continuously listens for incoming messages.

### Server Class (`Server.java`)

- Implements the server-side of the chat application.
- **Components**:
  - `JTextField`: For message input by the server.
  - `JPanel`: For displaying sent and received messages.
  - `DataOutputStream`: To send messages to the client.
- **Key Functions**:
  - `actionPerformed()`: Sends the text message when the "Send" button is clicked.
  - `formatLabel()`: Formats the outgoing message in a visually appealing format with a timestamp.
  - `main()`: Creates a `ServerSocket` to listen on a port, accepts client connections, and continuously listens for incoming messages from the client.

## How to Run

### Prerequisites

- Java Development Kit (JDK) installed.
- Basic knowledge of how to run Java programs from the command line or using an IDE like IntelliJ IDEA or Eclipse.

### Steps

1. **Compile** the `Client.java` and `Server.java` files:
   ```bash
   javac Client.java
   javac Server.java

Run the Server:

java Server
The server will start and wait for a connection from the client.

Run the Client:

java Client
The client will connect to the server running on localhost (IP address 127.0.0.1) and port 6001.

Chat: Type a message in the client window and press "Send." The message will be displayed in both the client and server windows.

Code Explanation
Sending Messages
When a message is typed and the "Send" button is pressed:
The message is captured from the JTextField.
It is formatted using formatLabel() to ensure proper spacing, background color, and width.
The message is displayed in the sender's chat window.
The message is sent to the other party (client or server) via the DataOutputStream.
Receiving Messages
Each side (client and server) continuously listens for incoming messages using a DataInputStream in a while loop.
When a message is received, it is displayed in the chat window of the recipient.
UI Design
The chat interface is designed using Swing components such as JPanel, JTextField, and JButton.
Custom icons and buttons are placed for added functionality, though they are currently non-functional.
Future Enhancements
Implement video and voice call functionality.
Add message encryption for secure communication.
Improve the UI design with additional features like message delivery statuses (sent, delivered, read).
Support for multiple clients (currently, it's designed for one-to-one communication).
