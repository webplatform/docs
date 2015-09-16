---
title: 'toLowerCase'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/es5c2d38(v=vs.94).aspx)'
compatibility:
  feature: toLowerCase
  topic: javascript
readiness: 'Ready to Use'
summary: 'Converts all the alphabetic characters in a string to lowercase.'
tags:
  - JS
  - Basic
uri: javascript/String/toLowerCase

---
## Summary

Converts all the alphabetic characters in a string to lowercase.

## Syntax

    strVariable.toLowerCase()

    "String Literal".toLowerCase()

## Examples

The following example demonstrates the effects of the **toLowerCase** method.

``` js
var str1 = "This is a STRING.";
var str2 = str1. toLowerCase();
document.write(str2);

// Output: this is a string.
```

## Remarks

The **toLowerCase** method has no effect on non-alphabetic characters.

## See also

### Other articles

-   [toLocaleLowerCase Method (String)](/javascript/String/toLocaleLowerCase)
-   [toUpperCase Method (String)](/javascript/String/toUpperCase)

