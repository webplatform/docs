---
title: slice
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns a new Blob object with bytes ranging from its optional start parameter up to but not including its optional end parameter.'
uri: apis/file/Blob/slice

---
# slice

## Summary

Returns a new Blob object with bytes ranging from its optional start parameter up to but not including its optional end parameter.

*Method of [apis/file/Blob](/apis/file/Blob)*

## Syntax

``` {.js}
var  = Blob.slice(start, end, contentType);
```

## Parameters

### start

 Data-typeÂ
:   Number

*(Optional)*

The optional start parameter is a value for the start point of a slice call, and is treated as a byte-order position, with position 0 representing the first byte. If start is negative, it is treated as length + start, where length is the length of the file (this allows byte selection starting from the end of the file).

If you specify a value for start that is larger than the size of the source Blob, the returned Blob has size 0 and contains no data.

### end

 Data-typeÂ
:   Number

*(Optional)*

The optional end parameter is a value for the end point of a slice call. The returned *slice* of data is up to but does not include the end byte. If end is omitted, **slice** selects all bytes from the start position to the end of the file. If end is negative, it is treated as length + end, where length is the length of the file (this allows byte selection starting from the end of the file).

### contentType

 Data-typeÂ
:   String

*(Optional)*

The optional contentType parameter is used to set a value (identical to one that is set with the HTTP/1.1 Content-Type header) on the [**Blob**](/apis/file/Blob) returned by the slice call.

## Return Value

Returns an object of type Blob.

A new Blob object containing the data in the specified range of bytes from the source Blob.

## Examples

This example creates a text blob object, reports its size, splits the blob object in half, reports that size, then closes the blob object.

``` {.js}
<script>
//create blob
var blobj = new Blob(["I scream, you scream, we all scream for ice cream!"], { "type"Â : "text/xml" });
alert("Blob size: " + blobj.size);
//slice blob in half, starting at beginning
var blobjfirsthalf = blobj.slice(0, Math.round(blobj.size/2));
alert("Blob first half size: " + blobjfirsthalf.size);
//close blob
blobj.close();
</script>
```

## Notes

The **slice** method returns a new [**Blob**](/apis/file/Blob) object with bytes ranging from the optional `start` parameter up to but not including the optional `end` parameter, and with a type attribute that is the value of the optional `contentType` parameter. If it is not possible to obtain the object in the range specified, your application should throw the `NotSupportedError` exception. For a code sample of the `slice` method, see [**Blob**](/apis/file/Blob).

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

