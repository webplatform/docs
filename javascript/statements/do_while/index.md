---
title: 'do while'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/5c1h7h0k(v=vs.94).aspx)'
compatibility:
  feature: 'do while'
  topic: javascript
readiness: 'Ready to Use'
summary: 'Executes a statement block once, and then repeats execution of the loop until a condition expression evaluates to false.'
tags:
  - JS
  - Basic
uri: 'javascript/statements/do while'

---
## Summary

Executes a statement block once, and then repeats execution of the loop until a condition expression evaluates to false.

## Syntax

    do {
        statement
    } while (expression) ;

**statement**
:   Required. The statement to be executed if expression is true. Can be a compound statement.

**expression**
:   Required. An expression that can be coerced to Boolean true or false. If expression is true , the loop is executed again. If expression is false , the loop is terminated.

## Examples

In the following example, the statements in the do...while loop continue to execute as long as the variable `i` is less than 10.

``` js
var i = 0;
 do {
     document.write(i + " ");
     i++;
 } while (i < 10);

 // Output: 0 1 2 3 4 5 6 7 8 9
```

In the following example, the statements inside the loop are executed once even though the condition is not met.

``` js
var i = 10;
 do {
     document.write(i + " ");
     i++;
 } while (i < 10);

 // Output: 10
```

## Remarks

Unlike the while statement, a do...while loop is executed one time before the conditional expression is evaluated.

On any line in a do...while block, you can use the break statement to cause the program flow to exit the loop, or you can use the continue statement to go directly to the while expression.

## See also

### Other articles

-   [break Statement](/javascript/statements/break)
-   [continue Statement](/javascript/statements/continue)
-   [for Statement](/javascript/statements/for)
-   [for...in Statement](/javascript/statements/for_in)
-   [while Statement](/javascript/statements/while)
-   [Labeled Statement](/javascript/statements/Labeled)

