---
title: 'encodeURIComponent'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/aeh9cef7(v=vs.94).aspx)'
compatibility:
  feature: encodeURIComponent
  topic: javascript
readiness: 'Ready to Use'
summary: 'Encodes a text string as a valid component of a Uniform Resource Identifier (URI).'
tags:
  - JS_Basic
uri: javascript/encodeURIComponent

---
## Summary

Encodes a text string as a valid component of a Uniform Resource Identifier (URI).

## Syntax

    encodeURIComponent( encodedURIString )

## Examples

The following code first encodes a URI component and then decodes it.

``` js
var uriEncode = encodeURIComponent ("www.Not a URL.com");
 var uriDecode = decodeURIComponent(uriEncode);

 document.write(uriEncode);
 document.write("<br/>");
 document.write(uriDecode);

 // Output:
 // www.Not%20a%20URL.com
 // www.Not a URL.com
```

## Remarks

The required encodedURIString argument is a value representing an encoded URI component.

The **encodeURIComponent** function returns an encoded URI. If you pass the result to **decodeURIComponent** , the original string is returned. Because the **encodeURIComponent** function encodes all characters, be careful if the string represents a path such as /folder1/folder2/default.html. The slash characters will be encoded and will not be valid if sent as a request to a web server. Use the **encodeURI** function if the string contains more than a single URI component.

## See also

### Other articles

-   [decodeURI Function](/javascript/decodeURI)
-   [decodeURIComponent Function](/javascript/decodeURIComponent)

