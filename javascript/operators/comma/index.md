---
title: comma
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'The comma operator (,) causes two expressions to be executed sequentially.'
uri: javascript/operators/comma

---
# comma

## Summary

The comma operator (,) causes two expressions to be executed sequentially.

## Syntax

    expression1 , expression2

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## Examples

The **,** operator causes the expressions to be executed in left-to-right order. A common use for the **,** operator is in the increment expression of a **for** loop. For example, the **for** statement allows only a single expression to be executed at the end of every pass through a loop. The **,** operator allows multiple expressions to be treated as a single expression, so both variables can be incremented.

``` {.js}
j=25;
for (i = 0; i < 10; i++, j++)
{
    k = i + j;
}
```

## See also

### Other articles

-   [for Statement](/javascript/statements/for)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9b37css7(v=vs.94).aspx)

