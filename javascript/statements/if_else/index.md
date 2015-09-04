---
title: if else
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
notes:
  - 'Todo: Probably should be renamed to "else if".'
summary: 'Conditionally executes a group of statements, depending on the value of an expression.'
uri: 'javascript/statements/if else'

---
# if else

## Summary

Conditionally executes a group of statements, depending on the value of an expression.

## Syntax

    if ( condition1 ) {
         statement1
    } else if ( condition2 ) {
         statement2
    } else {
         statement3
    }

**condition1**
:   Required. A Boolean expression. If condition1 is null or undefined , condition1 is treated as false.

**statement1**
:   Optional. The statement to be executed if condition1 is **true**. Can be a compound statement.

**condition2**
:   The condition to be evaluated.

**statement2**
:   Optional. The statement to be executed if condition2 is true. Can be a compound statement.

**statement3**
:   If both condition1 and condition2 are false , this statement is executed.

## Examples

The following code shows how to use if , if else , and else.

It is good practice to enclose statement1 and statement2 in braces ({}) for clarity and to avoid inadvertent errors.

``` {.js}
var z = 3;
 if (x == 5) {
     z = 10;
 }
 else if (x == 10) {
     z = 15;
 }
 else {
     z = 20;
 }
```

## See also

### Other articles

-   [Conditional (Ternary) Operator (?:)](/javascript/operators/conditional_ternary)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/85yyde5c(v=vs.94).aspx)

