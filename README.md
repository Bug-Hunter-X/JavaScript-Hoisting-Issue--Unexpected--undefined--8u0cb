# JavaScript Hoisting Bug

This repository demonstrates a common yet subtle error in JavaScript related to hoisting.  The code attempts to log the value of a variable *before* it's declared.  This results in unexpected behavior, printing `undefined` instead of throwing a ReferenceError as one might expect in other languages.  The solution illustrates how to correctly declare and initialize the variable.

## Bug

The `bug.js` file contains the problematic code.  Observe that the `console.log(a);` statement executes *before* `var a = 10;`.  Because of JavaScript's hoisting, the variable `a` is technically moved to the top of its scope, but it remains uninitialized, hence the `undefined` output.

## Solution

The `bugSolution.js` file shows the corrected code.  By ensuring that the variable `a` is declared and initialized *before* it's accessed, the expected output is achieved.