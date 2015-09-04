---
title: isFinite
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Determines whether a supplied number is finite.'
uri: javascript/isFinite

---
# isFinite

## Summary

Determines whether a supplied number is finite.

## Syntax

    isFinite(number)

**number**
:   Required. Any numeric value

## Return Value

Returns true if *number* is any value other than **NaN**, -Infinity or Infinity. In those three cases, it returns **false**.

## Examples

``` {.js}
isFinite(); // false, because its NaN
isFinite(42); // true
isFinite(-Infinity); //false
isFinite(4 / 0); //false
```

## See also

### Other articles

-   [isNaN Function](/javascript/isNaN)
-   [Infinity](/javascript/Infinity)
-   [NaN](/javascript/NaN)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/h5s8dazc(v=vs.94).aspx)

