# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. Specifically, the provided code attempts to parse a user ID from a route parameter as an integer without any validation.  If the ID is not a valid integer, the code will throw an error.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides a corrected version with proper error handling.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install express`
3. Run `node bug.js`
4. Access the route with an invalid ID (e.g., `/users/abc`).

The original code will either throw an error or produce unexpected results.

## Solution

The solution involves adding input validation to ensure the user ID is a number before attempting to parse it and using a `try...catch` block to gracefully handle errors that may occur during the parsing process.  See the `bugSolution.js` file for the corrected code.