---
title: bitwise not
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Performs a bitwise NOT (negation) on an expression.'
uri: 'javascript/operators/bitwise not'

---
# bitwise not

## Summary

Performs a bitwise NOT (negation) on an expression.

## Syntax

    result = ~ expression

**result**
:   Any variable.

**expression**
:   Any expression.

## Examples

See Remarks for explanation

``` {.js}
var temp = ~5;
//result is -6
```

## Remarks

All unary operators, such as the \~ operator, evaluate expressions as follows:

-   If applied to undefined or null expressions, a run-time error is raised.
-   Objects are converted to strings.
-   Strings are converted to numbers if possible. If not, a run-time error is raised.
-   Boolean values are treated as numbers (0 if false, 1 if true).

The operator is applied to the resulting number.

The \~ operator looks at the binary representation of the values of the expression and does a bitwise negation operation on it.

Any digit that is a 1 in the expression becomes a 0 in the result. Any digit that is a 0 in the expression becomes a 1 in the result.

The following example illustrates use of the bitwise NOT (\~) operator.

    var temp = ~5;

The resulting value is -6, as shown in the following table.

Expression
:   Binary value (two's complement)
5
:   00000000 00000000 00000000 00000101
\~5
:   11111111 11111111 11111111 11111010

## See also

### Other articles

-   [Logical NOT Operator (!)](/javascript/operators/logical_not)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/zf9s465t(v=vs.94).aspx)

