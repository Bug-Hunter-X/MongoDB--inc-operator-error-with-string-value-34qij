# MongoDB $inc operator error with string value

This repository demonstrates a common error when using the MongoDB `$inc` operator: attempting to increment a field with a string value instead of a number.

## Bug Description
The `$inc` operator is used to increment a numeric field.  However, if the field is not a number, or if a string value is provided to increment by, the operation will fail. This example shows that error, and how to fix it.  The error occurs because the `$inc` operator only works with numeric values. 

## Bug Solution
The solution involves ensuring that the field being incremented is of numeric type and providing a numeric value to increment by.  We'll modify the code to perform the operation correctly.

## How to reproduce the bug
1. Create a MongoDB collection named `myCollection` with a document containing a field named `count` that is initially a string.
2. Run the buggy code in the `bug.js` file.
3. Observe the error message indicating a type mismatch.

## How to fix the bug
1. Ensure the `count` field in your document is of numeric type (e.g., NumberInt or NumberLong).
2. Run the corrected code from the `bugSolution.js` file.