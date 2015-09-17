---
title: 'search'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/tbc7a78k(v=vs.94).aspx)'
compatibility:
  feature: search
  topic: javascript
readiness: 'Ready to Use'
summary: 'Finds the first substring match in a regular expression search.'
tags:
  - JS_Basic
uri: javascript/String/search

---
## Summary

Finds the first substring match in a regular expression search.

## Syntax

    stringObj.search( rgExp )

**stringObj**
:   Required. The String object or string literal on which to perform the search.

**rgExp**
:   Required. An instance of a **Regular Expression** object containing the regular expression pattern and applicable flags.

## Return Value

If a match is found, the **search** method returns an integer value that indicates the offset from the beginning of the string where the first match occurred. If no match is found, it returns -1.

## Examples

The following example illustrates the use of the **search** method.

``` js
var src = "is but a Dream within a dream";
 var re = /dream/;
 var pos = src.search(re);
 document.write(pos);
 document.write("<br/>");

 re = /dream/i;
 pos = src.search(re);
 document.write(pos);

 // Output:
 // 24
 // 9
```

## Remarks

You can also set the **i** flag that causes the search to be case-insensitive.

## See also

### Other articles

-   [exec Method (Regular Expression)](/javascript/regular_expression/exec)
-   [match Method (String)](/javascript/String/match)
-   [Regular Expression Object](/javascript/regular_expression)
-   [replace Method (String)](/javascript/String/replace)
-   [test Method (Regular Expression)](/javascript/regular_expression/test)

