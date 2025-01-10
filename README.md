# Node.js Server Hanging on Long Requests

This repository demonstrates a common issue in Node.js where a long-running request can cause the server to become unresponsive.  The problem stems from Node.js's single-threaded event loop.  If a request blocks the event loop for an extended period, no other requests can be processed.

**Problem:** The `server.js` file contains a simple HTTP server that simulates a long-running task (5 seconds). During this time, the server is unable to handle new requests.

**Solution:** The `server-solution.js` file provides a solution using asynchronous operations and a worker thread to prevent blocking the event loop.