# Incorrect $inc operator usage in MongoDB
This repository demonstrates a common error when using the `$inc` operator in MongoDB's `findOneAndUpdate` method.  Specifically, providing a string value to `$inc` instead of a number results in unexpected behavior. The `$inc` operator is designed to increment numerical values. When a string is provided, MongoDB performs string concatenation instead of numerical addition. 

## Bug
The `bug.js` file shows the problematic code using `$inc` with a string value.  This will cause the `count` field to become a string, resulting in unexpected behavior on subsequent increments.

## Solution
The `bugSolution.js` file demonstrates the corrected approach.  Ensure that the value passed to `$inc` is always a number.