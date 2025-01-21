# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler can block the event loop and make the server unresponsive.  The `server.js` file shows the problematic code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The original `server.js` uses a `while` loop to simulate a long-running task. This blocks the event loop, preventing the server from handling new requests during this period.  This is a classic example of how to inadvertently create a bottleneck and make your server unresponsive to clients.

## Solution

The `serverSolution.js` demonstrates the proper way to handle long-running operations.  It introduces asynchronous programming techniques to allow the server to remain responsive while the long task executes in the background.

## How to run the code

1. Clone this repository.
2. Navigate to the project directory.
3. Run the problematic code: `node server.js` 
4. Run the solution code: `node serverSolution.js`

You'll experience significantly better responsiveness with the solution. This highlights the importance of asynchronous programming in Node.js for maintaining performance and stability.