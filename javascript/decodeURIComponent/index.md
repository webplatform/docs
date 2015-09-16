---
title: 'decodeURIComponent'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/91b80x6x(v=vs.94).aspx)'
compatibility:
  feature: decodeURIComponent
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the unencoded version of an encoded component of a Uniform Resource Identifier (URI).'
tags:
  - JS
  - Basic
uri: javascript/decodeURIComponent

---
## Summary

Gets the unencoded version of an encoded component of a Uniform Resource Identifier (URI).

## Syntax

    decodeURIComponent( encodedURIString )

## Examples

The following code first encodes and then decodes a URI.

``` js
var uriEncode = encodeURI ("http://www.Not a URL.com");
 var uriDecode = decodeURIComponent(uriEncode);

 document.write (uriEncode);
 document.write("<br/>");
 document.write (uriDecode);

 // Output:
 // http://www.Not%20a%20URL.com
 // http://www.Not a URL.com
```

## Remarks

The required encodedURIString argument is a value representing an encoded URI component.

A URIComponent is part of a complete URI.

If the encodedURIString is not valid, a URIError occurs.

## See also

### Other articles

-   [decodeURI Function](/javascript/decodeURI)
-   [encodeURI Function](/javascript/encodeURI)

