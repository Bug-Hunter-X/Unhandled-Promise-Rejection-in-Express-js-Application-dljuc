# Unhandled Promise Rejection in Express.js
This repository demonstrates a common error in Express.js applications: unhandled promise rejections.  When asynchronous operations within request handlers fail, the application might not gracefully handle the error, leading to silent failures or crashes.

## Bug Description
The `bug.js` file contains an Express.js application with an asynchronous operation (`someAsyncOperation`).  If this operation fails, the error is logged to the console, but the response to the client is never sent, and the server doesn't gracefully handle the failure.

## Solution
The `bugSolution.js` file provides a corrected version. It includes comprehensive error handling using a `try...catch` block within the asynchronous operation or, alternatively, using `.catch()` to handle promise rejections.  This ensures that errors are appropriately handled, and the client receives a proper error response.