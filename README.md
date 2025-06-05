# Winsock TCP Client-Server Application (Windows)

Demonstrates a basic TCP client-server communication setup using the Winsock API on Windows. It includes functionality for secure port binding using `SO_EXCLUSIVEADDRUSE`.

## Features

* TCP client and server using Winsock2
* Secure port binding with `SO_EXCLUSIVEADDRUSE`
* Simple echo server: sends back received messages

## Files

* `server.cpp`: Sets up a TCP server that listens on a specified port, accepts client connections, and echoes back received messages.
* `client.cpp`: Connects to the server, sends a message, and prints the response.

## How to Build

### Prerequisites

* Windows OS (Done on Windows 11 64-bit)
* MinGW for compilation

### Compile:

```sh
g++ server.cpp -o server.exe -lws2_32
g++ client.cpp -o client.exe -lws2_32
```

## How to Run

### Run Server

```bash
\.server.exe
```

This starts the server and begins listening for incoming connections on port 27015.

### Run Client

```bash
\.client.exe localhost
```

This connects to the server running on localhost and sends a test message.

### Input: "hello" // from client.cpp

### Output:
```
Bytes Sent: 5
Bytes received: 5
Connection closed
```

## Security

### Port Binding

The server uses the `SO_EXCLUSIVEADDRUSE` socket option to prevent other applications from binding to the same port while the server is running.

### Communication

Currently, the communication is done over plain TCP. To secure the connection:

## License

This project is for educational purposes and is licensed under the MIT License.
