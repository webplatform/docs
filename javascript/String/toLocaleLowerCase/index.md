---
title: toLocaleLowerCase
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/94h6w1kx(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Converts all alphabetic characters to lowercase, taking into account the host environment''s current locale.'
tags:
  - JS
  - Basic
uri: javascript/String/toLocaleLowerCase

---
## <span>Summary</span>

Converts all alphabetic characters to lowercase, taking into account the host environment's current locale.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    stringVar.toLocaleLowerCase( )

## <span>Examples</span>

``` js
var hello = "wOrLd";
var foobar = hello.toLocaleLowerCase();
console.log(hello); // "wOrLd"
console.log(foobar); // "world"
```

## <span>Remarks</span>

The required stringVar reference is a String object or string literal.

The **toLocaleLowerCase** method converts the characters in a string, taking into account the host environment's current locale. In most cases, the result is the same as the result of the **toLowerCase** method. Results differ if the rules for a language conflict with the regular Unicode case mappings, such as Turkish.

## <span>See also</span>

### <span>Other articles</span>

-   [toLocaleUpperCase Method (String)](/javascript/String/toLocaleUpperCase)
-   [toLowerCase Method](/javascript/String/toLowerCase)

