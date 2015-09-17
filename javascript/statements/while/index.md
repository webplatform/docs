---
title: 'while'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/6wsy66x9(v=vs.94).aspx)'
compatibility:
  feature: while
  topic: javascript
readiness: 'Ready to Use'
summary: 'Executes a statement or series of statements while a specified condition is true.'
tags:
  - JS_Basic
uri: javascript/statements/while

---
## Summary

Executes a statement or series of statements while a specified condition is true.

## Syntax

    while ( expression ) {
      statements
    }

**expression**
:   Required. A Boolean expression that is checked before each iteration of the loop. If expression is true, the loop is executed. If expression is false, the loop is terminated.

**statements**
:   Optional. One or more statements to be executed if expression is true.

## Examples

``` js
var i = 0;

while (i < 5) {
  console.log("This runs 5 times");
  i++;
}
```

``` js
var i = 0;

while (i < 100) {
  if (i == 5) {
    // Stop the while loop early
    break;
  }
  console.log("This happens 5 times");
  i++;
}
```

## Usage

     The while statement checks the expression before a loop is first executed. If expression is false at this time, the loop is never executed.

The while statement keeps iterating until the conditional expression returns false, or encounters a break statement.

It's essential that the expression can become false or that that loop is terminated with the break statement to prevent an infinite loop.

## See also

### Other articles

-   [break Statement](/javascript/statements/break)
-   [continue Statement](/javascript/statements/continue)
-   [do...while Statement](/javascript/statements/do_while)
-   [for Statement](/javascript/statements/for)
-   [for...in Statement](/javascript/statements/for_in)

### Specification

-   [ECMAScript 5.1 (ECMA-262) - The while statement](http://www.ecma-international.org/ecma-262/5.1/#sec-12.6.2)

