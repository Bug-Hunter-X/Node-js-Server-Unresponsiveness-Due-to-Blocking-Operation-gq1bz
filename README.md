# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications: server unresponsiveness caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The provided server simulates a long-running task (a 5-second delay) within the request handler. This blocks the event loop, preventing the server from responding to further requests during that time.  This can lead to timeouts and an unresponsive server.

## Solution

The solution involves refactoring the code to use asynchronous operations (e.g., `setTimeout`) to avoid blocking the event loop. This ensures that the server remains responsive even during long-running tasks.  This approach is vital for maintaining the scalability and responsiveness of Node.js applications.