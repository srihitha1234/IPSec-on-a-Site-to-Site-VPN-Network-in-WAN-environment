# IPSec on a Site-to-Site VPN Network in WAN Environment

This project implements and optimizes IPSec (Internet Protocol Security) in a Site-to-Site VPN network for a WAN environment. IPSec ensures secure communication between geographically separated network nodes by providing high levels of data confidentiality, integrity, and authentication. This implementation uses socket programming in C and integrates OpenSSL for encryption and decryption.

Key features include:
- Secure data transmission using AES encryption.
- Implementation of IPSec protocols, including Authentication Header (AH) and Encapsulating Security Payload (ESP).
- Optimized algorithms for connection resiliency, failover, and selective traffic encryption.
- Multi-node VPN setup capability.

## Features
- **Tunneling**: Secure encapsulation of IP packets.
- **Encryption**: AES-based encryption and decryption for data confidentiality.
- **Authentication**: Pre-shared key mechanism for simple authentication.
- **Optimization**: 
  - Connection resiliency using failover and load balancing.
  - Selective traffic encryption for reduced processing overhead.
- **Multi-node Setup**: Support for WAN environments with multiple VPN nodes.

## Requirements
- GCC compiler
- OpenSSL library

## Usage

### Server
1. Compile the server code:
    ```bash
    gcc server.c -o server -lssl -lcrypto
    ```
2. Run the server:
    ```bash
    ./server
    ```

### Client
1. Compile the client code:
    ```bash
    gcc client.c -o client -lssl -lcrypto
    ```
2. Run the client with the server's IP and message:
    ```bash
    ./client <server_ip> "<message>"
    ```

### Example
- Server:
    ```bash
    ./server
    ```
- Client:
    ```bash
    ./client 127.0.0.1 "Hello, secure world!"
    ```
