---
title: concat
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns a string that contains the concatenation of two or more strings.'
uri: javascript/String/concat

---
# concat

## Summary

Returns a string that contains the concatenation of two or more strings.

## Syntax

    string1. concat([ string2 [, string3 [, . . . [, stringN ]]]])

**string1**
:   Required. The String object or string literal to which all other specified strings are concatenated.

**string2,. . ., stringN**
:   Optional. The strings to append to the end of string1.

## Examples

The following example illustrates the use of the **concat** method when used with a string:

``` {.js}
var str1 = "ABCD"
 var str2 = "EFGH";
 var str3 = "1234";
 var str4 = "5678";
 document.write(str1.concat(str2, str3, str4));

 // Output: "ABCDEFGH12345678"
```

## Remarks

The result of the **concat** method is equivalent to: result = string1 + string2 + string3 + stringN. A change of value in either a source or result string does not affect the value in the other string. If any of the arguments are not strings, they are first converted to strings before being concatenated to string1.

## See also

### Other articles

-   [Addition Operator (+)](/javascript/operators/addition)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/c751eb33(v=vs.94).aspx)

