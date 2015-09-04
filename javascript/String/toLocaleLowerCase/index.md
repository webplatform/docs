---
title: toLocaleLowerCase
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Converts all alphabetic characters to lowercase, taking into account the host environment''s current locale.'
uri: javascript/String/toLocaleLowerCase

---
# toLocaleLowerCase

## Summary

Converts all alphabetic characters to lowercase, taking into account the host environment's current locale.

## Syntax

    stringVar.toLocaleLowerCase( )

## Examples

``` {.js}
var hello = "wOrLd";
var foobar = hello.toLocaleLowerCase();
console.log(hello); // "wOrLd"
console.log(foobar); // "world"
```

## Remarks

The required stringVar reference is a String object or string literal.

The **toLocaleLowerCase** method converts the characters in a string, taking into account the host environment's current locale. In most cases, the result is the same as the result of the **toLowerCase** method. Results differ if the rules for a language conflict with the regular Unicode case mappings, such as Turkish.

## See also

### Other articles

-   [toLocaleUpperCase Method (String)](/javascript/String/toLocaleUpperCase)
-   [toLowerCase Method](/javascript/String/toLowerCase)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/94h6w1kx(v=vs.94).aspx)

