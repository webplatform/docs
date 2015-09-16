---
title: source
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/fkd8dws9(v=vs.94).aspx)'
notes:
  - 'Moved under javascript/RegExp'
readiness: 'Ready to Use'
summary: 'Returns a copy of the text of the regular expression pattern. Read-only. The rgExp argument is a Regular expression object. It can be a variable name or a literal.'
tags:
  0: JS
  1: Basic
  3: Property
uri: javascript/RegExp/source

---
## Summary

Returns a copy of the text of the regular expression pattern. Read-only. The rgExp argument is a Regular expression object. It can be a variable name or a literal.

## Syntax

    rgExp.source

## Examples

The following example illustrates the use of the **source** property:

``` js
function SourceDemo(re, s){
    var s1;
    // Test string for existence of regular expression.
    if (re.test(s))
       s1 = " contains ";
    else
       s1 = " does not contain ";
    // Get the text of the regular expression itself.
    return(s + s1 + re.source );
 }
```

## See also

### Other articles

-   [Regular Expression Object](/javascript/regular_expression)
-   [Regular Expression Object](/javascript/regular_expression)

