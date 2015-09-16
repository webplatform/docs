---
title: Uint32Array
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230737(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'A typed array of 32-bit unsigned integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.'
tags:
  - JS
  - Basic
uri: javascript/Uint32Array

---
## Summary

A typed array of 32-bit unsigned integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

## Syntax

<span class="language">JavaScript</span>

    uint32Array = new Uint32Array( length );

<span class="language">JavaScript</span>

    uint32Array = new Uint32Array( array );

<span class="language">JavaScript</span>

    uint32Array = new Uint32Array( buffer , byteOffset , length );

**uint32Array**
:   Required. The variable name to which the **Uint32Array** object is assigned.

**length**
:   Specifies the length (in bytes) of the array.

**array**
:   The array (or typed array) that is contained in this array. The contents are initialized to the contents of the given array or typed array, with each element converted to the Uint32 type.

**buffer**
:   The ArrayBuffer that the Uint32Array represents.

**byteOffset**
:   Optional. Specifies the offset in bytes from the start of the buffer at which the Uint32Array should begin.

**length**
:   The length of the array.

## Examples

The following example shows how to use a Uint32Array object to process the binary data acquired from an XMLHttpRequest:

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Uint32Array(buffer.byteLength / 4);
             for (var i = 0; i < ints.length; i++) {
                 ints[i] = dataview.getUint32(i * 4);
             }
         alert(ints[10]);
         }
     }
```

## Constants

The following table lists the constants of the **Uint32Array** object.

|Constant|Description|
|:-------|:----------|
|[BYTES\_PER\_ELEMENT Constant](/javascript/Uint32Array/BYTES_PER_ELEMENT)|The size in bytes of each element in the array.|

## Properties

The following table lists the constants of the **Uint32Array** object.

|Property|Description|
|:-------|:----------|
|[buffer Property](/javascript/Uint32Array/buffer)|Read-only. Gets the ArrayBuffer that is referenced by this array.|
|[byteLength Property](/javascript/Uint32Array/byteLength)|Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[byteOffset Property](/javascript/Uint32Array/byteOffset)|Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[length Property](/javascript/Uint32Array/length)|The length of the array.|

## Methods

The following table lists the methods of the **Uint32Array** object.

|Method|Description|
|:-----|:----------|
|[get Method](/javascript/Uint32Array/get)|Omittable. Gets the element at the specified index.|
|[set Method (Uint32Array)](/javascript/Uint32Array/set)|Sets a value or an array of values.|
|[subarray Method (Uint32Array)](/javascript/Uint32Array/subarray)|Gets a new Uint32Array view of the ArrayBuffer store for this array.|

