---
title: charCodeAt
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hza4d04f(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the Unicode value of the character at the specified location.'
tags:
  - JS
  - Basic
uri: javascript/String/charCodeAt

---
## <span>Summary</span>

Returns the Unicode value of the character at the specified location.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    strObj. charCodeAt( index )

**strObj**
:   Required. Any String object or string literal.

**index**
:   Required. The zero-based index of the desired character. If there is no character at the specified index, NaN is returned.

## <span>Examples</span>

The following example illustrates the use of the **charCodeAt** method.

``` js
var str = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
 document.write(str.charCodeAt(str.length - 1));

 // Output: 90
```

## <span>See also</span>

### <span>Other articles</span>

-   [String.fromCharCode Function](/javascript/String/fromCharCode)

