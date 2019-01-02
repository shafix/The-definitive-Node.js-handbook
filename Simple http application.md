# A simple Node.js http application

``` js
const http = require('http')
const hostname = '127.0.0.1'
const port = 3000
const server = http.createServer((req, res) => {
  res.statusCode = 200
  res.setHeader('Content-Type', 'text/plain')
  res.end('Hello World\n')
})
server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`)
})
```

The **createServer()** method of http creates a new HTTP server and returns it.

The server is set to listen on the specified port and hostname. When the server is ready, the callback function is called, in this case informing us that the server is running.

Whenever a **new request** is received, the **request event** is called, providing two objects: **a request (an http.IncomingMessageobject)** and a **response (an http.ServerResponseobject)**.

These 2 objects are essential to handle the HTTP call.

The first provides the **request details**. In this simple example, this is not used, but you could access the request headers and request data.

The second is used to **return data to the caller**.

In this case with: *res.statusCode = 200* , We set the statusCode property to 200, to indicate a successful response.

We set the Content-Type header: *res.setHeader('Content-Type', 'text/plain')* 

…and we end close the response, adding the content as an argument to end(): *res.end('Hello World\n')*
 
