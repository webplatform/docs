---
title: 'test'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/a55e5s6b(v=vs.94).aspx)'
compatibility:
  feature: test
  topic: javascript
notes:
  - 'Moved under javascript/RegExp'
readiness: 'Ready to Use'
summary: 'Returns a Boolean value that indicates whether or not a pattern exists in a searched string.'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/RegExp/test

---
## Summary

Returns a Boolean value that indicates whether or not a pattern exists in a searched string.

## Syntax

    rgExp.test( str )

**rgExp**
:   Required. An instance of a **Regular Expression** object containing the regular expression pattern and applicable flags.

**str**
:   Required. The string on which to perform the search.

## Examples

The following example illustrates the use of the **test** method. To use this example, pass the function a regular expression pattern and a string. The function will test for the occurrence of the regular expression pattern in the string and return a string indicating the results of that search:

``` js
function TestDemo(re, teststring)
 {
    // Test string for existence of regular expression.
    var found = re.test(teststring)

    // Format the output.
    var s = "";
    s += "'" + teststring + "'"

    if (found)
       s += " contains ";
    else
       s += " does not contain ";

    s += "'" + re.source + "'"
    return(s);
 }
```

## Remarks

The **test** method checks to see if a pattern exists within a string and returns **true** if so, and **false** otherwise.

The properties of the global **RegExp** object are not modified by the **test** method.

## See also

### Other articles

-   [RegExp Object](/javascript/RegExp)
-   [Regular Expression Object](/javascript/regular_expression)

