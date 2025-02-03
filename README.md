# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that arises when using `setTimeout` within a loop. The problem lies in how JavaScript handles closures and variable scoping. Each iteration of the loop shares the same `i` variable and its final value is used in all iterations after the 1 second delay.

## Bug

The `bug.js` file contains code that demonstrates the unexpected behavior. When the code is run, it logs the number 10 ten times, instead of logging the numbers 0 through 9 as one might expect.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  This solution uses an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring that each `setTimeout` callback captures its own copy of the `i` variable.

This example highlights the importance of understanding closures in JavaScript when working with asynchronous operations.