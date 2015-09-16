---
title: debugger
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/0bwt76sk(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Suspends execution.'
tags:
  - JS
  - Basic
uri: javascript/statements/debugger

---
## Summary

Suspends execution.

## Syntax

<span class="language">JavaScript</span>

    debugger

## Examples

This example uses the debugger statement to suspend execution for each iteration through the for loop.

**Note** -- To run this example, you must have a script debugger installed and the script must run in debug mode.Internet Explorer 8 includes the JavaScript debugger. If you are using an earlier version of Internet Explorer, see [How to: Enable and Start Script Debugging from Internet Explorer](http://go.microsoft.com/fwlink/?LinkId=133801).

``` js
for(i = 1; i<5; i++) {
    // Print i to the Output window.
    Debug.write("loop index is " + i);
    // Wait for user to resume.
    debugger
 }
```

## Remarks

You can place debugger statements anywhere in procedures to suspend execution. Using the debugger statement is similar to setting a breakpoint in the code.

The debugger statement suspends execution, but it does not close any files or clear any variables.

**Note** -- The debugger statement has no effect unless the script is being debugged.

## See also

### Other articles

-   [JavaScript Statements](/javascript/statements)

