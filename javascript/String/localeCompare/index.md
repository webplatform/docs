---
title: localeCompare
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Determines whether two strings are equivalent in the current locale.'
uri: javascript/String/localeCompare

---
# localeCompare

## Summary

Determines whether two strings are equivalent in the current locale.

## Syntax

    stringVar.localeCompare( stringExp )

**stringVar**
:   Required. A String object or string literal.

**stringExp**
:   Required. String to compare to stringVar.

## Examples

The following code shows how to use **localeCompare**.

``` {.js}
var str1 = "def";
 var str2 = "abc"

 document.write(str1.localeCompare(str2) + "<br/>");

 // Output: 1
 var str3 = "ghi";

 document.write(str1.localeCompare(str3)+ "<br/>");

 // Output: -1
 var str4 = "def";

 document.write(str1.localeCompare(str4));

 // Output: 0
```

## Remarks

The **localeCompare** performs a locale-sensitive string comparison of the stringVar and the stringExp and returns -1, 0, or +1, depending on the sort order of the system default locale.

If stringVar sorts before stringExp , **localeCompare** returns -1; if stringVar sorts after stringExp , +1 is returned. A return value of zero means that the two strings are equivalent.

## See also

### Other articles

-   [toLocaleString Method (Object)](/javascript/Object/toLocaleString)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/62b7ahzy(v=vs.94).aspx)

