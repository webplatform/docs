---
title: encodeURI
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Encodes a text string as a valid Uniform Resource Identifier (URI)'
uri: javascript/encodeURI

---
# encodeURI

## Summary

Encodes a text string as a valid Uniform Resource Identifier (URI)

## Syntax

    encodeURI( URIString )

## Examples

The following code first encodes and then decodes a URI.

``` {.js}
var uriEncode = encodeURI ("http://www.Not a URL.com");
 var uriDecode = decodeURIComponent(uriEncode);

 document.write(uriEncode);
 document.write("<br/>");
 document.write(uriDecode);

 // Output:
 // http://www.Not%20a%20URL.com
 // http://www.Not a URL.com
```

## Remarks

The required URIString argument is a value representing an encoded URI.

The **encodeURI** function returns an encoded URI. If you pass the result to **decodeURI** , the original string is returned. The **encodeURI** function does not encode the following characters: ":", "/", ";", and "?". Use **encodeURIComponent** to encode these characters.

## See also

### Other articles

-   [decodeURI Function](/javascript/decodeURI)
-   [decodeURIComponent Function](/javascript/decodeURIComponent)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/xh9be5xc(v=vs.94).aspx)

