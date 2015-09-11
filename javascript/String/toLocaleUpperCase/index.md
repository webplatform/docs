---
title: toLocaleUpperCase
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/6t6xaca8(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a string where all alphabetic characters have been converted to uppercase, taking into account the host environment''s current locale.'
tags:
  - JS
  - Basic
uri: javascript/String/toLocaleUpperCase

---
## <span>Summary</span>

Returns a string where all alphabetic characters have been converted to uppercase, taking into account the host environment's current locale.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    stringVar.toLocaleUpperCase( )

## <span>Examples</span>

``` js
var hello = "wOrLd";
var foobar = hello.toLocaleUpperCase();
console.log(hello); // "wOrLd"
console.log(foobar); // "WORLD"
```

## <span>Remarks</span>

The required stringVar reference is a String object or string literal.

The **toLocaleUpperCase** method converts the characters in a string, taking into account the host environment's current locale. In most cases, the result is the same as the result the **toUpperCase** method. Results differ if the rules for a language conflict with the regular Unicode case mappings, such as Turkish.

## <span>See also</span>

### <span>Other articles</span>

-   [toLocaleLowerCase Method (String)](/javascript/String/toLocaleLowerCase)
-   [toUpperCase Method (String)](/javascript/String/toUpperCase)

