---
title: test
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/a55e5s6b(v=vs.94).aspx)'
notes:
  - 'Moved under javascript/RegExp'
readiness: 'Ready to Use'
summary: 'Returns a Boolean value that indicates whether or not a pattern exists in a searched string.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/RegExp/test

---
## <span>Summary</span>

Returns a Boolean value that indicates whether or not a pattern exists in a searched string.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    rgExp.test( str )

**rgExp**
:   Required. An instance of a **Regular Expression** object containing the regular expression pattern and applicable flags.

**str**
:   Required. The string on which to perform the search.

## <span>Examples</span>

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

## <span>Remarks</span>

The **test** method checks to see if a pattern exists within a string and returns **true** if so, and **false** otherwise.

The properties of the global **RegExp** object are not modified by the **test** method.

## <span>See also</span>

### <span>Other articles</span>

-   [RegExp Object](/javascript/RegExp)
-   [Regular Expression Object](/javascript/regular_expression)

