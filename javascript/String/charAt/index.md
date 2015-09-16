---
title: charAt
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/65zt5h10(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the character at the specified index.'
tags:
  - JS
  - Basic
uri: javascript/String/charAt

---
## Summary

Returns the character at the specified index.

## Syntax

    strObj. charAt( index )

**strObj**
:   Required. Any String object or string literal.

**index**
:   Required. The zero-based index of the desired character.

## Examples

The following example illustrates the use of the **charAt** method:

``` js
var str = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
 document.write(str.charAt(str.length - 1));

 // Output: Z
```

## Remarks

The **charAt** method returns a character value equal to the character at the specified index. The first character in a string is at index 0, the second is at index 1, and so forth. Values of index that are out of range return an empty string.

## See also

### Other articles

-   [String Object](/javascript/String)

