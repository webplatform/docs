---
title: Infinity
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'A number that is larger than the largest floating point number.'
uri: javascript/Infinity

---
# Infinity

## Summary

A number that is larger than the largest floating point number.

## Syntax

    Infinity

## Return Value

Returns an initial value of **Number.POSITIVE\_INFINITY**.

## Examples

Divisions by zero will give you Infinity. Divisions by negative zero will give you -Infinity.

``` {.js}
42 / 0; // Infinity
42 / 0; // -Infinity
```

Everything beyond Infinity remains Infinity

``` {.js}
Infinity * Infinity; // Infinity
```

If an arithmetic overflow occurs, Infinity is also returned

``` {.js}
Math.pow(2, 1024); // Infinity
```

## Remarks

The **Infinity** constant is a member of the **Global** object, and is made available when the scripting engine is initialized.

## Notes

## Negative Infinity

Negative Infinity (-Infinity) is smaller than the smallest floating point number and returns a value of **Number.NEGATIVE\_INFINITY**.

## Mathematical

This value behaves mathematically like infinity; for example, anything multiplied by Infinity is Infinity, and anything divided by Infinity is 0.

Infinity subtracted by Infinity will return **NaN**

## isFinite()

The [isFinite()](/javascript/isFinite) function can be used to check if a given value is a finite number

## See also

### Other articles

-   [Number](/javascript/Number)
-   [Number Constants](/javascript/Number/constants)
-   [isFinite()](/javascript/isFinite)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/kddt5x39(v=vs.94).aspx)

