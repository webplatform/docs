---
title: 'Blob'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Blob](https://developer.mozilla.org/en-US/docs/DOM/Blob) Article]'
  - 'Microsoft Developer Network: [[blob constructor](http://msdn.microsoft.com/en-us/library/ie/hh673542(v=vs.85).aspx#blobbuilder) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The Blob object represents immutable raw data. It provides a method to slice data objects between ranges of bytes into further chunks of raw data.'
tags:
  - API_Objects
  - API
  - FileAPI
uri: apis/file/Blob

---
## Summary

The Blob object represents immutable raw data. It provides a method to slice data objects between ranges of bytes into further chunks of raw data.

## Overview

**Blob** provides an attribute representing the size of the chunk of data. The [**File**](/apis/file/File) object inherits from the **Blob** object. **Blob** objects can be read asynchronously only on the main thread via [**FileReader**](/apis/file/FileReader) objects, but metadata access via attributes such as **size** and **type** return synchronously (this trade-off is based on the underlying assumption that metadata access will not significantly block or disrupt the browser's main thread, whereas reading **Blob** data will).

## Properties

*No properties.*

## Methods

[close](/apis/file/Blob/close)
:   Releases the file lock for the associated file resource or frees the memory for the Blob object. After calling this method, performing addition operations on the Blob object fails and throws an exception.

[slice](/apis/file/Blob/slice)
:   Returns a new Blob object with bytes ranging from its optional start parameter up to but not including its optional end parameter.

## Events

*No events.*

## Examples

// Example for creating a URL to a typed array using a blob

``` js
var typedArray = GetTheTypedArraySomehow();
var blob = new Blob([typedArray], {type: "application/octet-binary"}); // pass a useful mime type here
var url = URL.createObjectURL(blob);
// url will be something like: blob:d3958f5c-0777-0845-9dcf-2cb28783acaf
// now you can use the url in any context that regular URLs can be used in, for example img.src, etc.
```

// Blob constructor example usage

``` js
var aFileParts = ['<a id="a"><b id="b">hey!</b></a>'];
var oMyBlob = new Blob(aFileParts, { "type" : "text/xml" }); // the blob
```

## Related specifications

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## See also

### Other articles

[Saving files locally using Blob and msSaveBlob](http://msdn.microsoft.com/en-us/library/ie/hh779016(v=vs.85).aspx)
