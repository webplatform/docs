---
title: 'decodeURI'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ht8a077w(v=vs.94).aspx)'
compatibility:
  feature: decodeURI
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the unencoded version of an encoded Uniform Resource Identifier (URI).'
tags:
  - JS_Basic
uri: javascript/decodeURI

---
## Summary

Gets the unencoded version of an encoded Uniform Resource Identifier (URI).

## Syntax

    decodeURI( URIstring )

## Examples

The following code first encodes a URI component and then decodes it.

``` js
var uriEncode = encodeURIComponent ("www.Not a URL.com");
 var uriDecode = decodeURIComponent(uriEncode);

 document.write (uriEncode);
 document.write ("<br/>");
 document.write (uriDecode);

 // Output:
 // www.Not%20a%20URL.com
 // www.Not a URL.com
```

## Remarks

The required URIstring argument is a value representing an encoded URI.

Use the **decodeURI** function instead of the deprecated **unescape** function.

The **decodeURI** function returns a string value.

If the URIString is not valid, a URIError occurs.

**Applies To** : [Global Object](/javascript/Global)

## See also

### Other articles

-   [decodeURIComponent Function](/javascript/decodeURIComponent)
-   [encodeURI Function](/javascript/encodeURI)
-   [Global Object](/javascript/Global)

