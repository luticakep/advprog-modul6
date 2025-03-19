# Module 6

## Commit 1 Reflection notes: Handling connection and checking response
This Rust project implements a simple HTTP server that listens on 127.0.0.1:7878. The `handle_connection` function reads incoming requests line by line from a TcpStream and prints them in the terminal. Through this exercise, I learned how Rust ensures memory safety in network programming and how raw HTTP requests are structured. 

## Commit 2 Reflection notes: Returning HTML
![Optional alt text](assets/reflection2.png)
In this commit, I added a simple HTML response to the server. The `handle_connection` function now writes an HTTP response to the TcpStream, which includes a status line, headers, and a body. Through this exercise, I learned the importance of accurately specifying headers—especially the Content-Length—to ensure the client can correctly display the page. This experience also highlights how Rust’s safety guarantees and straightforward I/O handling make it simpler to serve dynamic or static content in a custom web server.