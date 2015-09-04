---
title: close
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Releases the file lock for the associated file resource or frees the memory for the Blob object. After calling this method, performing addition operations on the Blob object fails and throws an exception.'
uri: apis/file/Blob/close

---
# close

## Summary

Releases the file lock for the associated file resource or frees the memory for the Blob object. After calling this method, performing addition operations on the Blob object fails and throws an exception.

*Method of [apis/file/Blob](/apis/file/Blob)*

## Syntax

``` {.js}
 Blob.close();
```

## Return Value

No return value

## Examples

This example creates a text blob object, reports its size, splits the blob object in half, reports that size, then closes the blob object.

``` {.js}
<script>
//create blob
var blobj = new Blob(["I scream, you scream, we all scream for ice cream!"], { "type" : "text/xml" });
alert("Blob size: " + blobj.size);
//slice blob in half, starting at beginning
var blobjfirsthalf = blobj.slice(0, Math.round(blobj.size/2));
alert("Blob first half size: " + blobjfirsthalf.size);
//close blob
blobj.close();
</script>
```

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

