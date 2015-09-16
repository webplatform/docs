---
title: Float32Array
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212916(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'A typed array of 32-bit float values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.'
tags:
  - JS
  - Basic
uri: javascript/Float32Array

---
## Summary

A typed array of 32-bit float values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

## Syntax

<span class="language">JavaScript</span>

    float32Array = new Float32Array( length );

<span class="language">JavaScript</span>

    float32Array = new Float32Array( array );

<span class="language">JavaScript</span>

    float32Array = new Float32Array( buffer , byteOffset , length );

**float32Array**
:   Required. The variable name to which the **Float32Array** object is assigned.

**length**
:   Specifies the length (in bytes) of the array.

**array**
:   The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Float32 type.

**buffer**
:   The ArrayBuffer that the Float32Array represents.

**byteOffset**
:   Optional. Specifies the offset in bytes from the start of the buffer at which the Float32Array should begin.

**length**
:   The length of the array.

## Examples

The following example shows how to use a Float32Array object to process the binary data acquired from an XmlHttpRequest:

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Float32Array(buffer.byteLength / 4);
             for (var i = 0; i < ints.length; i++) {
                 ints[i] = dataview.getFloat32(i * 4);
             }
         alert(ints[10]);
         }
     }
```

## Constants

The following table lists the constants of the **Float32Array** object.

|Constant|Description|
|:-------|:----------|
|[BYTES\_PER\_ELEMENT Constant](/javascript/Float32Array/BYTES_PER_ELEMENT)|The size in bytes of each element in the array.|

## Properties

The following table lists the constants of the **Float32Array** object.

|Property|Description|
|:-------|:----------|
|[buffer Property](/javascript/Float32Array/buffer)|Read-only. Gets the ArrayBuffer that is referenced by this array.|
|[byteLength Property](/javascript/Float32Array/byteLength)|Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[byteOffset Property](/javascript/Float32Array/byteOffset)|Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[length Property](/javascript/Float32Array/length)|The length of the array.|

## Methods

The following table lists the methods of the **Float32Array** object.

|Method|Description|
|:-----|:----------|
|[get Method](/javascript/Float32Array/get)|Omittable. Gets the element at the specified index.|
|[set Method (Float32Array)](/javascript/Float32Array/set)|Sets a value or an array of values.|
|[subarray Method (Float32Array)](/javascript/Float32Array/subarray)|Gets a new Float32Array view of the ArrayBuffer store for this array.|

