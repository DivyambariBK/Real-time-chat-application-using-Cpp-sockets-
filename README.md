# Chat Application with Group and Private Messaging 💬
*Sasken Internship Program-2025*
## 🎯 Project Goal
This project implements a **Terminal-Based Multi-Client Chat Application** using **TCP Sockets** and **Multithreading** in **C++**. The primary objective is to allow multiple clients to communicate with each other in real-time through group and private messages, while also maintaining a chat history log on the server side.

---
## 📌 Project Overview
This project is a **Terminal-based Chat Application** built using **C++**, designed to facilitate:
- ✅ Group Chat
- ✅ Private Messaging using `/pm` command
- ✅ Group Creation and Assignment using `/group` command
- ✅ Server-Side Logging of all Chat Activities
- ✅ Real-time Multi-User Chatting via TCP Sockets

It is a simple and effective demonstration of **Socket Programming**, **Multi-threading**, and **File Logging** in Linux environments.

---
## ⚙️ How the Project Works

### 1. **Server-Side Logic**
- The server program listens on a specific port (`10000`) for incoming client connections.
- Once a client connects, the server creates a **dedicated thread** for each client using `std::thread`, ensuring simultaneous communication with multiple clients.
- Each client has an associated `Client` structure, which contains:
  - Client ID
  - Username
  - Socket Descriptor
  - Group Name (optional)
  - Thread Handler
- The server supports:
  - **Broadcast Messaging**: Sends messages to all connected clients.
  - **Group Messaging**: Sends messages only to clients within the same group.
  - **Private Messaging**: Sends messages to a specific client.
  - **Chat Logging**: Records all events and messages in `chat_log.txt` for traceability.

### 2. **Client-Side Logic**
- Upon connecting, the client enters their username.
- Clients can:
  - Send general messages (broadcasted to all).
  - Join/create a group using `/group groupname`.
  - Send private messages using `/pm username message`.
  - Leave the chat using `#exit`.
- Multithreading is used to handle **sending** and **receiving** messages concurrently to provide a smooth, real-time chat experience.

---

## 🛠️ Technical Concepts Used

| Concept               | Description |
|------------------------|-------------|
| **TCP Sockets**       | Enables reliable, two-way communication between server and multiple clients. |
| **Multithreading**    | `std::thread` is used to handle multiple clients simultaneously without blocking the server. |
| **Mutex Locks**       | `std::mutex` ensures thread safety when accessing shared resources like client lists and console outputs. |
| **File I/O**          | Logs chat messages and events in `chat_log.txt` using file streams. |
| **Terminal Colors**   | Improves readability using ANSI escape codes for colored outputs. |

---

## 💡 Example Chat Flow

- Client1 joins and types: `Hello everyone!`
    - Server broadcasts it to all clients.
- Client2 types: `/group tech`
    - Client2 is now part of group "tech".
- Client2 types: `Hello tech group!`
    - Message is visible only to members of "tech".
- Client1 sends: `/pm Client2 Hey, quick chat?`
    - Private message sent to Client2 only.
- Server keeps a log of all these actions in `chat_log.txt`.
---
## 📌 Conclusion

This project demonstrates a simple yet functional terminal-based chat application built using C++ and socket programming. It includes features such as:

- ✅ **Group Chat** — Users can create and join chat groups using simple commands.
- ✅ **Private Messaging** — Directly message any connected user using the `/pm` command.
- ✅ **Chat Logging** — All chats are automatically logged into `chat_log.txt` for future reference.
- ✅ **Color-coded Messages** — Each user is assigned a unique color to enhance readability.
- ✅ **Thread-based Concurrency** — The server handles multiple clients simultaneously using threads.

This project is an excellent learning resource for understanding multithreading, socket communication, and client-server architecture in C++. It can be further extended with advanced features like file sharing, authentication, and a graphical interface.

---
