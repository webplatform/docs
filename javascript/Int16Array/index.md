---
title: Int16Array
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212480(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'A typed array of 16-bit integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.'
tags:
  - JS
  - Basic
uri: javascript/Int16Array

---
## Summary

A typed array of 16-bit integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

## Syntax

    int16Array = new Int16Array( length );

    int16Array = new Int16Array( array );

    int16Array = new Int16Array( buffer , byteOffset , length );

**int16Array**
:   Required. The variable name to which the **Int16Array** object is assigned.

**length**
:   Specifies the length (in bytes) of the array.

**array**
:   The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Int16 type.

**buffer**
:   The ArrayBuffer that the Int16Array represents.

**byteOffset**
:   Optional. Specifies the offset in bytes from the start of the buffer at which the Int16Array should begin.

**length**
:   The length of the array.

## Examples

The following example shows how to use an Int16Array object to process the binary data acquired from an XmlHttpRequest:

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Int16Array(buffer.byteLength / 2);
             for (var i = 0; i < ints.length; i++) {
                 ints[i] = dataview.getInt16(i * 2);
             }
         alert(ints[10]);
         }
     }
```

## Constants

The following table lists the constants of the **Int16Array** object.

|Constant|Description|
|:-------|:----------|
|[BYTES\_PER\_ELEMENT Constant](/javascript/Int16Array/BYTES_PER_ELEMENT)|The size in bytes of each element in the array.|

## Properties

The following table lists the constants of the **Int16Array** object.

|Property|Description|
|:-------|:----------|
|[buffer Property](/javascript/Int16Array/buffer)|Read-only. Gets the ArrayBuffer that is referenced by this array.|
|[byteLength Property](/javascript/Int16Array/byteOffset)|Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[byteOffset Property](/javascript/Int8Array/byteOffset)|Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[length Property](/javascript/Float32Array/length)|The length of the array.|

## Methods

The following table lists the methods of the **Int16Array** object.

|Method|Description|
|:-----|:----------|
|[get Method](/javascript/Int16Array/get)|Omittable. Gets the element at the specified index.|
|[set Method (Int16Array)](/javascript/Int16Array/set)|Sets a value or an array of values.|
|[subarray Method (Int16Array)](/javascript/Int16Array/subarray)|Gets a new Int16Array view of the ArrayBuffer store for this array.|

