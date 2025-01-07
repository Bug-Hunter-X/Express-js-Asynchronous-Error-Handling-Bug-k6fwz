# Express.js Asynchronous Error Handling Bug

This repository demonstrates a common bug in Express.js applications related to asynchronous error handling.  When an error occurs within an asynchronous callback, the server might crash if not handled properly.

## Bug Description

The `bug.js` file contains an Express.js server with a route that simulates an asynchronous operation.  There's a 50% chance of an error being thrown. If the error is not properly handled, the server crashes. 

The solution in `bugSolution.js` demonstrates how to use error handling middleware to gracefully handle these asynchronous errors.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js`.  Refresh the page several times to observe the crashing behavior.
4. Run `node bugSolution.js`. The server should handle errors gracefully without crashing.

## Solution

The solution involves using error-handling middleware.  The correct usage is shown in `bugSolution.js`.  It ensures that any errors thrown during request processing are caught and handled appropriately, preventing the server from crashing.