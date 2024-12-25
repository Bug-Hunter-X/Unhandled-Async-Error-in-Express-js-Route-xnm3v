# Unhandled Async Error in Express.js

This repository demonstrates a common error in Express.js applications: unhandled errors within asynchronous route handlers.  Asynchronous operations (like database queries, API calls, or file I/O) can throw errors that, if not properly caught, will crash the server.

The `bug.js` file showcases an example of this.  The `bugSolution.js` file provides a solution using error handling middleware.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install Express.js.
4. Run `node bug.js` to start the server.
5. Make several requests to the server (`http://localhost:3000`).  You'll notice the server will crash after a certain number of requests.

## Solution

The `bugSolution.js` file demonstrates how to correctly handle asynchronous errors using Express.js error handling middleware. This ensures that the server doesn't crash even if errors occur during asynchronous operations.