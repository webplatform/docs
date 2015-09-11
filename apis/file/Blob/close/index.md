---
title: close
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/file/Blob
    href: /apis/file/Blob
standardization_status: 'W3C Working Draft'
summary: 'Releases the file lock for the associated file resource or frees the memory for the Blob object. After calling this method, performing addition operations on the Blob object fails and throws an exception.'
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
uri: apis/file/Blob/close

---
## <span>Summary</span>

Releases the file lock for the associated file resource or frees the memory for the Blob object. After calling this method, performing addition operations on the Blob object fails and throws an exception.

Method of [apis/file/Blob](/apis/file/Blob)[apis/file/Blob](/apis/file/Blob)

## <span>Syntax</span>

``` js
 Blob.close();
```

## <span>Return Value</span>

No return value

## <span>Examples</span>

This example creates a text blob object, reports its size, splits the blob object in half, reports that size, then closes the blob object.

``` js
<script>
//create blob
var blobj = new Blob(["I scream, you scream, we <b>all</b> scream for ice cream!"], { "type" : "text/xml" });
alert("Blob size: " + blobj.size);
//slice blob in half, starting at beginning
var blobjfirsthalf = blobj.slice(0, Math.round(blobj.size/2));
alert("Blob first half size: " + blobjfirsthalf.size);
//close blob
blobj.close();
</script>
```

## <span>Related specifications</span>

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
