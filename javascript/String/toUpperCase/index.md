---
title: 'toUpperCase'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/kk06d70k(v=vs.94).aspx)'
compatibility:
  feature: toUpperCase
  topic: javascript
readiness: 'Ready to Use'
summary: 'Converts all the alphabetic characters in a string to uppercase.'
tags:
  - JS_Basic
uri: javascript/String/toUpperCase

---
## Summary

Converts all the alphabetic characters in a string to uppercase.

## Syntax

    strVariable.toUpperCase()

    "String Literal".toUpperCase()

## Examples

The following example demonstrates the effects of the **toUpperCase** method:

``` js
var str1 = "This is a STRING.";
 var str2 = str1.toUpperCase();
 document.write(str2);

 // Output: THIS IS A STRING.
```

## Remarks

The **toUpperCase** method has no effect on non-alphabetic characters.

## See also

### Other articles

-   [toLocaleUpperCase Method (String)](/javascript/String/toLocaleUpperCase)
-   [toLowerCase Method](/javascript/String/toLowerCase)

