# Express.js Route Handler Error

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the route `/users/:id` does not handle the case where `req.params.id` is not a valid integer, leading to potential crashes or unexpected behavior.

## Bug

The `bug.js` file contains the erroneous code. The handler attempts to parse `req.params.id` as an integer using `parseInt()`, but it doesn't check for the case where the parsing fails (e.g., `req.params.id` is a string that cannot be converted to an integer).

## Solution

The `bugSolution.js` file shows the corrected code.  It includes comprehensive error handling to check if `userId` is a valid integer and to handle the case where a user with the given ID is not found.