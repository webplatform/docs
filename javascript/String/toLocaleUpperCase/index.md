---
title: toLocaleUpperCase
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns a string where all alphabetic characters have been converted to uppercase, taking into account the host environment''s current locale.'
uri: javascript/String/toLocaleUpperCase

---
# toLocaleUpperCase

## Summary

Returns a string where all alphabetic characters have been converted to uppercase, taking into account the host environment's current locale.

## Syntax

    stringVar.toLocaleUpperCase( )

## Examples

``` {.js}
var hello = "wOrLd";
var foobar = hello.toLocaleUpperCase();
console.log(hello); // "wOrLd"
console.log(foobar); // "WORLD"
```

## Remarks

The required stringVar reference is a String object or string literal.

The **toLocaleUpperCase** method converts the characters in a string, taking into account the host environment's current locale. In most cases, the result is the same as the result the **toUpperCase** method. Results differ if the rules for a language conflict with the regular Unicode case mappings, such as Turkish.

## See also

### Other articles

-   [toLocaleLowerCase Method (String)](/javascript/String/toLocaleLowerCase)
-   [toUpperCase Method (String)](/javascript/String/toUpperCase)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/6t6xaca8(v=vs.94).aspx)

