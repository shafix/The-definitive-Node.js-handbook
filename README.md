# Overview
Node.js is a runtime environment for JavaScript that runs on the server.
It is built on top of the Google Chrome V8 JavaScript engine, and it’s mainly used to create web servers.

**It’s fast** - JavaScript code running on Node.js (depending on the benchmark) can be twice as fast as compiled languages like C or Java, and orders of magnitude faster than interpreted languages like Python or Ruby, because of its non-blocking paradigm.

### It’s an asynchronous platform

In traditional programming languages (C, Java, Python, PHP) all instructions are blocking by default unless you explicitly “opt in” to perform asynchronous operations. If you perform a network request to read some JSON, the execution of that particular thread is blocked until the response is ready.

JavaScript allows to create **asynchronous** and **non-blocking** code in a very simple way, by **using a single thread**, callback functions and **event-driven programming**. Every time an expensive operation occurs, we pass a callback function that will be called once we can continue with the processing. We’re not waiting for that to finish before going on with the rest of the program.

This allows Node.js to handle **thousands of concurrent connections with a single server** without introducing the burden of managing threads concurrency, which would be a major source of bugs.

Node provides **non-blocking I/O primitives**, and generally, libraries in Node.js are written using non-blocking paradigms, making a **blocking behavior an exception rather than the normal**.

When Node.js needs to perform an I/O operation, like reading from the network, access a database or the filesystem, instead of blocking the thread **Node.js will simply resume the operations when the response comes back**, instead of wasting CPU cycles waiting.


