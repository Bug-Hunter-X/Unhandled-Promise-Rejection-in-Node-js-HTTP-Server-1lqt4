# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js: unhandled promise rejections in asynchronous HTTP servers.  Unhandled rejections can lead to silent failures and crashes, making debugging difficult.  The `bug.js` file shows an example of a server with an unhandled rejection. The `bugSolution.js` shows how to properly handle such rejections.

## How to reproduce the bug

1. Clone this repository.
2. Run `node bug.js`.  The server will start, but might fail silently if the simulated error occurs.

## How to fix the bug

1. Examine the `bugSolution.js` file for the corrected implementation.
2. The key is to use a `.catch()` block to handle potential errors within the promise chain.

## Key Learning

Always handle promise rejections within your asynchronous operations, particularly within long-running servers, to prevent unexpected crashes and ensure robust application behavior.