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
