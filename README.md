# Express.js Route Handler Bug
This repository demonstrates a common bug in Express.js route handlers: missing error handling for invalid input and non-specific error responses.

## Bug Description
The `bug.js` file contains an Express.js route handler that fetches a user by ID.  It has two critical flaws:

1. **Missing input validation:** It doesn't handle cases where the `userId` is not a number, which can lead to unexpected errors or crashes.
2. **Generic error responses:** If a user is not found (404), it returns a generic 404 response without providing details about the cause of the error (e.g., invalid ID).

## Solution
The `bugSolution.js` file provides an improved version of the route handler. It includes input validation to check if `userId` is a number and returns more informative error responses.