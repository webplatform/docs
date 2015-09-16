---
title: try catch finally
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/4yahc5d8(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets up blocks of code in which errors that are thrown in one block are handled in another. Errors that are thrown inside the try block are caught in the catch block. JavaScript.'
tags:
  - JS
  - Basic
uri: 'javascript/statements/try catch finally'

---
## Summary

Sets up blocks of code in which errors that are thrown in one block are handled in another. Errors that are thrown inside the try block are caught in the catch block. JavaScript.

## Syntax

<span class="language">JavaScript</span>

    try {
      tryStatements
    } catch ( exception ) {
      catchStatements
    } finally {
      finallyStatements
    }

**tryStatements**
:   Required. Statements where an error can occur.

**exception**
:   Required. Any variable name. The initial value of exception is the value of the thrown error.

**catchStatements**
:   Optional. Statements to handle errors occurring in the associated tryStatements.

**finallyStatements**
:   Optional. Statements that are unconditionally executed after all other error processing has occurred.

## Examples

``` js
try {
  functionDoesNotExist();
}
catch (e) {
  console.log(e.message);
  // "functionDoesNotExist is not defined"
}

console.log("This code runs!");
// This runs because the error was successfully caught
```

## Usage

     The try...catch...finally statement provides a way to handle some or all of the errors that may occur in a given block of code, while still running code. If errors occur that are not handled, JavaScript provides the normal error message.

The try block contains code that may provoke an error, while the catch block contains the code that handles some or all errors. If an error occurs in the try block, program control is passed to the catch block. The value of exception is the value of the error that occurred in the try block. If no error occurs, the code in the catch block is never executed.

You can pass the error up to the next level by using the throw statement to re-throw the error.

After all the statements in the try block have been executed and error handling has been done in the catch block, the statements in the finally block are executed, whether or not an error was handled. The code in the finally block is guaranteed to run unless an unhandled error occurs (for example, a run-time error inside the **catch** block).

## See also

### Other articles

-   [throw Statement](/javascript/statements/throw)

### Specification

-   [ECMAScript 5.1 (ECMA-262) - The try statement](http://www.ecma-international.org/ecma-262/5.1/#sec-12.14)

