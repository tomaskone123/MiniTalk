Here's the updated `README.md` with the instructions for running the server and client in two different terminals:

```markdown
# MiniTalk

MiniTalk is a simple project that demonstrates communication between two programs using signals. The project consists of a server and a client, which communicate by sending and receiving data through UNIX signals.

## Overview

MiniTalk allows you to send a message from one program to another using signals. The client sends a message, which is received and processed by the server. This project is designed to help you understand the basics of inter-process communication (IPC) using signals in C.

## How It Works

1. **Client:** The client program sends a string message to the server by sending a series of signals (SIGUSR1 and SIGUSR2).
2. **Server:** The server listens for signals and reconstructs the message sent by the client.
3. **Signal Communication:** The server receives each signal as a bit (either 0 or 1) and reconstructs the complete message bit by bit.

## Requirements

- GCC (GNU Compiler Collection)
- Linux-based operating system

## Usage

### Compilation

To compile the project, run the following command:

```bash
make
```

This will generate two executables: `server` and `client`.

### Running the Server

1. Open a terminal and start the server by running:

```bash
./server
```

2. The server will wait for incoming messages. It must be running in one terminal before you can send a message from the client.

### Running the Client

1. Open a **second terminal** and run the client:

```bash
./client <server_pid> <message>
```

Where:
- `<server_pid>` is the PID of the server (you can get this by running `ps aux | grep server`).
- `<message>` is the message you want to send to the server.

**Important:** Make sure to run the server and client in **two separate terminals**. The server must be running first to receive the signals from the client.



Now the README includes clear instructions to run both the server and client in separate terminals.
