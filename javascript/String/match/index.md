---
title: match
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Matches a string with a regular expression, and returns an array containing the results of that search.'
uri: javascript/String/match

---
# match

## Summary

Matches a string with a regular expression, and returns an array containing the results of that search.

## Syntax

    stringObj.match( rgExp )

**stringObj**
:   Required. The String object or string literal on which to perform the search.

**rgExp**
:   Required. A regular expression object that contains the regular expression pattern and applicable flags. This can also be a variable name or string literal containing the regular expression pattern and flags.

## Examples

The following example illustrates the use of the match method.

``` {.js}
var src = "azcafAJAC";

 var re = /[a-c]/;

 var result = src.match(re);

 // The entire match is in array element 0.
 document.write(result[0] + "<br/>");

 // Now try the same match with the global flag.
 var reg = /[a-c]/g;
 result = src.match(reg);


 // The matches are in elements 0 through n.
 for (var index = 0; index < result.length; index++)
 {
     document.write ("submatch " + index + ": " +  result[index]);
     document.write("<br />");
 }
```

## Remarks

If the **match** method does not find a match, it returns null. If it finds a match, **match** returns an array, and the properties of the global **RegExp** object are updated to reflect the results of the match.

The array returned by the **match** method has three properties, **input** , **index** and **lastIndex**. The input property contains the entire searched string. The index property contains the position of the matched substring within the complete searched string. The **lastIndex** property contains the position following the last character in the last match.

If the global flag ( **g** ) is not set, Element zero of the array contains the entire match, while elements 1 through n contain any submatches. This behavior is the same as the behavior of the [exec Method (Regular Expression)](/javascript/regular_expression/exec) when the global flag is not set. If the global flag is set, elements 0 through n contain all matches that occurred.

If the flag **i** is set, the search is not case-sensitive.

## See also

### Other articles

-   [exec Method (Regular Expression)](/javascript/regular_expression/exec)
-   [RegExp Object](/javascript/RegExp)
-   [Regular Expression Object](/javascript/regular_expression)
-   [replace Method (String)](/javascript/String/replace)
-   [search Method (String)](/javascript/String/search)
-   [test Method (Regular Expression)](/javascript/regular_expression/test)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7df7sf4x(v=vs.94).aspx)

