-----TCP Chat Application in C++-----
A simple and scalable TCP-based chat application written in C++ using WinSock2 for Windows. This project supports both one-to-one and one-to-many communication, allowing a single server to handle multiple clients via multithreading.

🚀 Features
📡 Socket Programming with WinSock2 API
🤝 Client-Server Communication
🧵 Multi-threaded Server to handle concurrent clients
📨 Real-time message broadcast to all connected clients
💬 Clean separation of sending and receiving threads on the client-side
✅ Works on Windows systems with basic setup

🛠️ Tech Stack
   Language: C++
   API: WinSock2
   OS: Windows
   Threads: std::thread for concurrent handling

📁 Project Structure
📦 TCP-Chat-CPP
 ┣ 📄 server.cpp      // Server code handling multiple clients
 ┣ 📄 client.cpp      // Client code to send/receive messages
 ┗ 📄 README.md       // Project documentation

📌 How It Works
🖥️ Server
 -Initializes socket and binds to IP/port.
 -Listens for incoming connections.
 -For every connected client, spawns a new thread to:
 -Receive messages
 -Broadcast them to other clients
 -Cleans up closed sockets.

👤 Client
 -Connects to server.
 -Prompts user for a name.
 -Runs two threads:
 -One to send messages
 -One to receive messages
 -Sends "exit" to leave the chat.

✅ Getting Started
1. Prerequisites
   Windows OS
   C++ compiler (MSVC or MinGW)
   Enable Winsock2 with #pragma comment(lib, "ws2_32.lib")

2. Compile & Run
    Server
    bash
    Copy
    Edit
    g++ server.cpp -o server.exe -lws2_32
    ./server.exe
    Client
    bash
    Copy
    Edit
    g++ client.cpp -o client.exe -lws2_32
   ./client.exe
⚠️ Make sure to run the server first, then start one or more clients.

🧪 Demo
Coming soon: Screenshots or terminal output of a live chat session.

📎 Use Cases
-Educational demonstration of TCP and threading
-Base for building chat, multiplayer games, or client-server applications
