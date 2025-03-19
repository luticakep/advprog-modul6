# Module 6

## Commit 1 Reflection notes: Handling connection and checking response
This Rust project implements a simple HTTP server that listens on 127.0.0.1:7878. The `handle_connection` function reads incoming requests line by line from a TcpStream and prints them in the terminal. Through this exercise, I learned how Rust ensures memory safety in network programming and how raw HTTP requests are structured. 

## Commit 2 Reflection notes: Returning HTML
![Optional alt text](assets/reflection2.png)
In this commit, I added a simple HTML response to the server. The `handle_connection` function now writes an HTTP response to the TcpStream, which includes a status line, headers, and a body. Through this exercise, I learned the importance of accurately specifying headers—especially the Content-Length—to ensure the client can correctly display the page. This experience also highlights how Rust’s safety guarantees and straightforward I/O handling make it simpler to serve dynamic or static content in a custom web server.

## Commit 3 Reflection notes: Validating request and selectively responding
![Optional alt text](assets/reflection3.png)
In this commit, I added a conditional response to the server. The `handle_connection` function now checks if the incoming request is a GET request for the root path and responds with a 200 OK status code and the HTML content. If the request is for any other path, the server responds with a 404 Not Found status code and sends a `404.html`. This exercise helped me understand how to parse and validate HTTP requests in Rust and how to send appropriate responses based on the request type. It also demonstrated how Rust’s pattern matching and error handling features can be used to write clean and concise code.