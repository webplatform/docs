---
title: lastIndexOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/6d20k718(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the last occurrence of a substring in the string.'
tags:
  - JS
  - Basic
uri: javascript/String/lastIndexOf

---
## Summary

Returns the last occurrence of a substring in the string.

## Syntax

<span class="language">JavaScript</span>

    strObj.lastIndexOf( substring [, startindex ] )

**strObj**
:   Required. A String object or string literal.

**substring**
:   Required. The substring to search for.

**startindex**
:   Optional. The index at which to begin searching. If omitted, the search begins at the end of the string.

## Examples

The **lastIndexOf** method returns an integer value indicating the beginning of the substring within the String object. If the substring is not found, a -1 is returned.

If startindex is negative, startindex is treated as zero. If it is larger than the greatest character position index, it is treated as the largest possible index.

Searching is performed starting at the last character in the string. Otherwise, this method is identical to **indexOf**.

The following example illustrates the use of the **lastIndexOf** method.

``` js
var str = "time, time";

var s = "";
s += "time is at position " + str.lastIndexOf("time");
s += "<br />";
s += "abc is at position " + str.lastIndexOf("abc");

document.write(s);

// Output:
// time is at position 6
// abc is at position -1
```

## See also

### Other articles

-   [indexOf Method (String)](/javascript/String/indexOf)

