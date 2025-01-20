# Node.js Port Already in Use Error

This repository demonstrates a common error in Node.js: attempting to start a server on a port that is already in use.

## Bug
The `bug.js` file contains a simple HTTP server that attempts to listen on port 8080. If this port is already occupied by another process (e.g., another Node.js server or a different application), the server will fail to start and throw an error.

## Solution
The `bugSolution.js` file provides a solution to this problem by using the `server.on('error', ...)` event listener to gracefully handle port binding errors.  This approach prevents the application from crashing, logs an informative message, and may even attempt to listen on an alternative port.