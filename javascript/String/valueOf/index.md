---
title: valueOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155295(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the value of a string.'
tags:
  - JS
  - Basic
uri: javascript/String/valueOf

---
## Summary

Returns the value of a string.

## Syntax

<span class="language">JavaScript</span>

    string.valueOf()

## Return Value

Returns the string value.

## Examples

In the following example, the string object is the same as the return value.

``` js
var str = "every good boy does fine";
var strStr = str.valueOf();

if (str === strStr)
document.write("same");
else
document.write("different");

// Output:
// same
```

