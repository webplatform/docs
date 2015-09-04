---
title: indexOf
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns the position of the first occurrence of a substring.'
uri: javascript/String/indexOf

---
# indexOf

## Summary

Returns the position of the first occurrence of a substring.

## Syntax

    strObj. indexOf( subString [, startIndex ])

**strObj**
:   Required. A String object or string literal.

**subString**
:   Required. The substring to search for in the string

**startIndex**
:   Optional. The index at which to begin searching the String object. If omitted, search starts at the beginning of the string.

## Examples

The following example illustrates the use of the **indexOf** method.

``` {.js}
var str = "original equipment manufacturer";

 var s = "equip is at position " + str.indexOf("equip");
 s += "<br />";
 s += "abc is at position " + str.indexOf("abc");

 document.write(s);

 // Output:
 // equip is at position 9
 // abc is at position -1
```

## Remarks

The **indexOf** method returns the beginning of the substring in the String object. If the substring is not found, -1 is returned.

If startindex is negative, startindex is treated as zero. If it is greater than the highest index, it is treated as the highest index.

Searching is performed from left to right. Otherwise, this method is identical to **lastIndexOf**.

## See also

### Other articles

-   [lastIndexOf Method (String)](/javascript/String/lastIndexOf)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/53xtt423(v=vs.94).aspx)

