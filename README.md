

# ChatRoom Application with WebSocket

## Overview

This project implements a simple ChatRoom application using WebSocket technology in Java. It allows multiple users to connect to a chat room and exchange messages in real-time.

## Components

1. **Controller**
   - The Controller class handles HTTP requests and WebSocket connections. It manages WebSocket sessions and message handling between clients.

2. **WebSocketConfig**
   - The WebSocketConfig class configures WebSocket endpoints and message handlers. It defines the WebSocket endpoint URL and configures message buffers and timeouts.

3. **WebProvider**
   - The WebProvider class provides utility methods and configurations for the web application. It may include settings for CORS (Cross-Origin Resource Sharing) and other web-related configurations.

4. **ChatMessage**
   - The ChatMessage class represents a message exchanged between clients in the chat room. It includes fields like sender, content, timestamp, etc., to encapsulate message data.

5. **MessageType (Enum)**
   - The MessageType enum defines different types of messages that can be exchanged, such as CHAT, JOIN, LEAVE, etc. Each type corresponds to a specific action or event in the chat room.

## Setup and Deployment

### Requirements
- Java Development Kit (JDK) version X or above
- Apache Maven (for dependency management)

### Installation

1. Clone the repository to your local machine:
   ```
   git clone https://github.com/your/repository.git
   ```

2. Build the project using Maven:
   ```
   mvn clean install
   ```

### Running the Application

1. Run the application using Maven:
   ```
   mvn spring-boot:run
   ```

2. Access the application at `http://localhost:8080` (or the configured port).

## Usage

- Connect multiple clients to `ws://localhost:8080/chatroom` using WebSocket.
- Send messages in JSON format with appropriate message types (CHAT, JOIN, LEAVE).
- Example message format:
  ```json
  {
    "type": "CHAT",
    "sender": "Alice",
    "content": "Hello, everyone!"
  }
  ```




