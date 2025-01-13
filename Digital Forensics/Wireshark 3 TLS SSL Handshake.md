The TLS (Transport Layer Security) handshake is a process that establishes a secure communication session between a client (e.g., a web browser) and a server. It ensures confidentiality, integrity, and authenticity. Here's a brief overview of the key steps:
![Screenshot 2025-01-13 003735](https://github.com/user-attachments/assets/9f654d1d-7715-4f45-b474-bc750717c963)
I used wireshark to display the handshake between my client pc and google.ca as the server
![Screenshot 2025-01-13 003240](https://github.com/user-attachments/assets/68672d63-7073-4797-b0e1-a40406382794)


First both server acknowledge each other
![Screenshot 2025-01-13 003313](https://github.com/user-attachments/assets/091f725a-4900-4811-a3cd-30521a4bf126)




Client Hello:

The client sends a "hello" message to the server, including supported TLS versions, cipher suites, and a randomly generated number.
Server Hello:

The server responds with its chosen TLS version, cipher suite, another random number, and its digital certificate (containing its public key).
![Screenshot 2025-01-13 003338](https://github.com/user-attachments/assets/4d4a74fc-9a34-422d-80db-4eb1458c82aa)
