---
title: for
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/s1cyybdf(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Executes a block of statements for as long as a specified condition is true.'
tags:
  - JS
  - Basic
uri: javascript/statements/for

---
## Summary

Executes a block of statements for as long as a specified condition is true.

## Syntax

    for ([ initialization ]; [ test ]; [ increment ]) {
        statement
    }

**initialization**
:   Optional. An expression. This expression is executed only once, before the loop is executed.

**test**
:   Optional. A Boolean expression. If test is true , statement is executed. If test if false , the loop is terminated.

**increment**
:   Optional. An expression. The increment expression is executed at the end of every pass through the loop.

**statement**
:   Optional. One or more statements to be executed if test is **true**. Can be a compound statement.

## Examples

In the following example, the for statement executes the enclosed statements as follows:

-   First, the initial value of the variable `i` is evaluated.
-   Then, as long as the value of `i` is less than or equal to 9, the `document.write` statements are executed and `i` is reevaluated.
-   When `i` is greater than 9, the condition becomes false and control is transferred outside the loop.

``` js
// i is set to 0 at the start and is incremented by 1 at the
 // end of each iteration.
 // The loop terminates when i is not less than or equal to
 // 9 before a loop iteration.
 for (var i = 0; i <= 9; i++) {
    document.write (i);
    document.write (" ");
 }

 // Output: 0 1 2 3 4 5 6 7 8 9
```

All of the expressions of the for statement are optional. In the following example, the for statements create an infinite loop, and a break statement is used to exit the loop.

``` js
var j = 0;
 for (;;) {
     if (j >= 5) {
         break;
     }
     j++;
     document.write (j + " ");
 }

 // Output: 1 2 3 4 5
```

## Remarks

You usually use a for loop when the loop is to be executed a known number of times. A for loop is useful for iterating over arrays and for performing sequential processing.

The test of a conditional expression occurs before the execution of the loop, so a for statement executes zero or more times.

On any line in a for loop statement block, you can use the break statement to exit the loop, or you can use the continue statement to transfer control to the next iteration of the loop.

## See also

### Other articles

-   [for...in Statement](/javascript/statements/for_in)
-   [while Statement](/javascript/statements/while)

