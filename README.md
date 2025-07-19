# 💬 Multi-Client Chat Application (Sasken Internship 2025)

A **multi-client chatroom application** built using **C++ socket programming** as part of the **Sasken Internship 2025** project. This project demonstrates the use of basic **TCP/IP socket programming**, **multithreading**, and **client-server architecture** using **Linux OS**.

---

## 📌 Features
✅ Multiple clients can chat together  
✅ One central server handles all clients  
✅ Real-time messaging  
✅ Clean and simple command-line interface  
✅ Efficient use of multithreading  
✅ Graceful handling of client disconnection  

---

## 🛠️ Tech Stack
- **Language**: C++  
- **OS**: Linux (Tested on Ubuntu)  
- **Networking API**: Berkeley Sockets (sys/socket.h)  
- **Multithreading**: pthreads  
- **Compiler**: g++  

---

## ⚙️ How it works
- The **server** creates a TCP socket and listens on a specified port.
- Multiple **clients** can connect to the server using TCP connections.
- Each client is handled in a separate **thread** on the server.
- Any message sent by a client is **broadcasted to all other clients**.
- Server handles client disconnections gracefully without crashing.

---

## 📌 Compilation & Execution

### 🖥️ On Linux

#### Compile Server:
```bash
g++ server.cpp -o server -pthread
```

#### Compile Client:
```bash
g++ client.cpp -o client -pthreadd
```

#### 🖥️ Run Server:
```bash
./server
```
####🖥️ Run Client:
```bash
./client
```
---
### 🎁 Expected Learning Outcomes
- ✅ Practical exposure to client-server architecture.
- ✅ Hands-on experience in C++ socket programming.
- ✅ Understanding of multithreading and resource synchronization.
- ✅ Insight into real-time communication systems used in the industry.

---
### 📝 Conclusion
The Multi-Client Chat Application, developed as part of the Sasken Internship 2025, demonstrates the application of low-level networking concepts using C++ and sockets. This project simulates the working principles of a basic chatroom application by integrating socket programming and multithreading, providing practical exposure to how real-time communication systems operate in industry.

