---
title: 'fromCharCode'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/wb4w0k66(v=vs.94).aspx)'
compatibility:
  feature: fromCharCode
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns a string from a number of Unicode character values.'
tags:
  - JS
  - Basic
uri: javascript/String/fromCharCode

---
## Summary

Returns a string from a number of Unicode character values.

## Syntax

    String.fromCharCode([ code1 [, code2 [, ...[, codeN ]]]])

**String**
:   Required. The String object.

**code1 , . . . , codeN**
:   Optional. A series of Unicode character values to convert to a string. If no arguments are supplied, the result is the empty string.

## Examples

You call this function on the String object rather than on a string instance.

The following example shows how to use this method:

``` js
var test = String.fromCharCode(112, 108, 97, 105, 110);
document.write(test);

// Output: plain
```

## See also

### Other articles

-   [charCodeAt Method (String)](/javascript/String/charCodeAt)

