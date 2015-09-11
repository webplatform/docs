---
title: split
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/t5az126b(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Split a string into substrings using the specified separator and return the substrings as an array.'
tags:
  - JS
  - Basic
uri: javascript/String/split

---
## <span>Summary</span>

Split a string into substrings using the specified separator and return the substrings as an array.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    stringObj.split([separator[, limit ]])

**stringObj**
:   Required. The String object or string literal to be split. This object is not modified by the **split** method.

**separator**
:   Optional. A string or a **Regular Expression** object that identifies character or characters to use in separating the string. If omitted, a single-element array containing the entire string is returned.

**limit**
:   Optional. A value used to limit the number of elements returned in the array.

## <span>Return Value</span>

The result of the **split** method is an array of strings split at each point where separator occurs in stringObj. The separator is not returned as part of any array element.

## <span>Examples</span>

The following example illustrates the use of the **split** method.

``` js
var s = "The quick brown fox jumps over the lazy dog.";
 var ss = s.split(" ");
 for (i in ss) {
     document.write(ss[i];
     document.write("<br/>");
 }

 // Output:
 // The
 // quick
 // brown
 // fox
 // jumps
 // over
 // the
 // lazy
 // dog.
```

## <span>See also</span>

### <span>Other articles</span>

-   [concat Method (String)](/javascript/String/concat)
-   [RegExp Object](/javascript/RegExp)
-   [Regular Expression Object](/javascript/regular_expression)

