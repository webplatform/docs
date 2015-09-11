---
title: localeCompare
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/62b7ahzy(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Determines whether two strings are equivalent in the current locale.'
tags:
  - JS
  - Basic
uri: javascript/String/localeCompare

---
## <span>Summary</span>

Determines whether two strings are equivalent in the current locale.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    stringVar.localeCompare( stringExp )

**stringVar**
:   Required. A String object or string literal.

**stringExp**
:   Required. String to compare to stringVar.

## <span>Examples</span>

The following code shows how to use **localeCompare**.

``` js
var str1 = "def";
 var str2 = "abc"

 document.write(str1.localeCompare(str2) + "<br/>");

 // Output: 1
 var str3 = "ghi";

 document.write(str1.localeCompare(str3)+ "<br/>");

 // Output: -1
 var str4 = "def";

 document.write(str1.localeCompare(str4));

 // Output: 0
```

## <span>Remarks</span>

The **localeCompare** performs a locale-sensitive string comparison of the stringVar and the stringExp and returns -1, 0, or +1, depending on the sort order of the system default locale.

If stringVar sorts before stringExp , **localeCompare** returns -1; if stringVar sorts after stringExp , +1 is returned. A return value of zero means that the two strings are equivalent.

## <span>See also</span>

### <span>Other articles</span>

-   [toLocaleString Method (Object)](/javascript/Object/toLocaleString)

