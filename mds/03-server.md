# Sever

## What is a server? 

- A `server` is a computer system or a software program that provides functionality or resources to other computers or programs, typically over a network. It serves requests from client devices, such as computers, smartphones, or other servers, by responding to those requests with the required resources or data.

## Basic Node server:

```js
const http = require("http");

const fs = require("fs");
const PORT = 3000;

const server = http.createServer(function (req, res) {
  res.writeHead(200, { "content-type": "text/html" });
  fs.createReadStream("index.html").pipe(res);
});
server.listen(PORT);
console.log(`Server started on port ${PORT}`);

```

....
