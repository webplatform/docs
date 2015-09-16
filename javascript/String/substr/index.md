---
title: substr
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/0esxc5wy(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets a substring beginning at the specified location and having the specified length.'
tags:
  - JS
  - Basic
uri: javascript/String/substr

---
## Summary

Gets a substring beginning at the specified location and having the specified length.

## Syntax

<span class="language">JavaScript</span>

    stringvar.substr( start [, length ])

**stringvar**
:   Required. A string literal or String object from which the substring is extracted.

**start**
:   Required. The starting position of the desired substring. The index of the first character in the string is zero.

**length**
:   Optional. The number of characters to include in the returned substring.

## Examples

The following example illustrates the use of the **substr** method.

``` js
var s = "The quick brown fox jumps over the lazy dog.";
 var ss = s.substr(10, 5);
 document.write("[" + ss + "] <br>");

 ss = s.substr(10);
 document.write("[" + ss + "] <br>");

 ss = s.substr(10, -5);
 document.write("[" + ss + "] <br>");

ss = s.substr(-4);
document.write("[" + ss + "] <br>");
 // Output:
 // [brown]
 // [brown fox jumps over the lazy dog.]
 // []
 // [dog.]
```

## Remarks

If length is zero or negative, an empty string is returned. If not specified, the substring continues to the end of stringvar. If start is negative, it is treated as [stringvar.length+start] if length is omitted this would return the last \`start\` characters of the stringvar.

## See also

### Other articles

-   [substring Method (String)](/javascript/String/substring)

