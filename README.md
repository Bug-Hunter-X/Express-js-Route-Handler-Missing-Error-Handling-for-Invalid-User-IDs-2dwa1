# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input parameters.

The `bug.js` file contains a route handler that fetches a user by ID. It uses `parseInt` to convert the ID to an integer, but fails to handle cases where the ID is not a valid integer (e.g., a string or a non-numeric value). This can lead to unexpected errors and crashes.

The `bugSolution.js` file demonstrates how to fix this issue by adding proper error handling using `isNaN` to check for invalid input and returning a user-friendly 404 error when no user is found.