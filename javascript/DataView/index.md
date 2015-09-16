---
title: 'DataView'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212463(v=vs.94).aspx)'
compatibility:
  feature: DataView
  topic: javascript
readiness: 'Ready to Use'
summary: 'You can use a DataView object to read and write the different kinds of binary data to any location in the ArrayBuffer.'
tags:
  - JS
  - Basic
uri: javascript/DataView

---
## Summary

You can use a DataView object to read and write the different kinds of binary data to any location in the ArrayBuffer.

## Syntax

    dataView = new DataView( DataView( buffer , byteOffset , byteLength ));

**dataView**
:   Required. The variable name to which the **DataView** object is assigned.

**buffer**
:   The ArrayBuffer that the DataView represents.

**byteOffset**
:   Optional. Specifies the offset in bytes from the start of the buffer at which the DataView should begin.

**byteLength**
:   Optional. Specifies the length (in bytes) of the section of the buffer that the DataView should represent.

## Examples

The following example shows how to use a DataView object to process the binary data acquired from an XmlHttpRequest:

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var ints = new Int32Array(dataView.byteLength / 4);
             for (var i = 0; i < ints.length; i++) {
                 ints[i] = dataview.getInt32(i * 4);
             }
         alert(ints[10]);
         }
     }
```

## Remarks

If both byteOffset and byteLength are omitted, the DataView spans the entire ArrayBuffer range. If the byteLength is omitted, the DataView extends from the given byteOffset until the end of the ArrayBuffer. If the given byteOffset and byteLength references an area beyond the end of the ArrayBuffer, an exception is raised.

## Properties

The following table lists the properties of the **DataView** object.

|Property|Description|
|:-------|:----------|
|[buffer Property](/javascript/DataView/buffer)|Read-only. Gets the ArrayBuffer that is referenced by this view.|
|[byteLength Property](/javascript/DataView/byteLength)|Read-only. The length of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[byteOffset Property](/javascript/DataView/byteOffset)|Read-only. The offset of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.|

## Methods

The following table lists the methods of the **DataView** object.

|Method|Description|
|:-----|:----------|
|[getInt8 Method](/javascript/DataView/getInt8)|Gets the Int8 value at the specified byte offset from the start of the view.|
|[getUint8 Method (DataView)](/javascript/DataView/getUint8)|Gets the Uint8 value at the specified byte offset from the start of the view.|
|[getInt16 Method (DataView)](/javascript/DataView/getInt16)|Gets the Int16 value at the specified byte offset from the start of the view.|
|[getUint16 Method (DataView)](/javascript/DataView/getUint16)|Gets the Uint16 value at the specified byte offset from the start of the view.|
|[getInt32 Method (DataView)](/javascript/DataView/getInt32)|Gets the Int32 value at the specified byte offset from the start of the view.|
|[getUint32 Method (DataView)](/javascript/DataView/getUint32)|Gets the Uint32 value at the specified byte offset from the start of the view.|
|[getFloat32 Method (DataView)](/javascript/DataView/getFloat32)|Gets the Float32 value at the specified byte offset from the start of the view.|
|[getFloat64 Method (DataView)](/javascript/DataView/getFloat64)|Gets the Float64 value at the specified byte offset from the start of the view.|
|[setInt8 Method (DataView)](/javascript/DataView/setInt8)|Stores a Int8 value at the specified byte offset from the start of the view.|
|[setUint8 Method (DataView)](/javascript/DataView/setUint8)|Stores a Uint8 value at the specified byte offset from the start of the view.|
|[setInt16 Method (DataView)](/javascript/DataView/setInt16)|Stores a Int16 value at the specified byte offset from the start of the view.|
|[setUint16 Method (DataView)](/javascript/DataView/setUint16)|Stores a Uint16 value at the specified byte offset from the start of the view.|
|[setInt32 Method (DataView)](/javascript/DataView/setInt32)|Stores a Int32 value at the specified byte offset from the start of the view.|
|[setUint32 Method (DataView)](/javascript/DataView/setUint32)|Stores a Uint32 value at the specified byte offset from the start of the view.|
|[setFloat32 Method (DataView)](/javascript/DataView/setFloat32)|Stores a Float32 value at the specified byte offset from the start of the view.|
|[setFloat64 Method (DataView)](/javascript/DataView/setFloat64)|Stores a Float64 value at the specified byte offset from the start of the view.|

