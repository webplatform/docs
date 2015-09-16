---
title: 'Uint8Array'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212477(v=vs.94).aspx)'
compatibility:
  feature: Uint8Array
  topic: javascript
readiness: 'Ready to Use'
summary: 'A typed array of 8-bit unsigned integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.'
tags:
  - JS
  - Basic
uri: javascript/Uint8Array

---
## Summary

A typed array of 8-bit unsigned integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

## Syntax

    uint8Array = new Uint8Array( length );

    uintArray = new Uint8Array( array );

    uintArray = new Uint8Array( buffer , byteOffset , length );

**uint8Array**
:   Required. The variable name to which the **Uint8Array** object is assigned.

**length**
:   Specifies the length (in bytes) of the array.

**array**
:   The array (or typed array) that is contained in this array. The contents are initialized to the contents of the given array or typed array, with each element converted to the Uint8 type.

**buffer**
:   The ArrayBuffer that the Uint8Array represents.

**byteOffset**
:   Optional. Specifies the offset in bytes from the start of the buffer at which the Uint8Array should begin.

**length**
:   The length of the array.

## Examples

The following example shows how to use a Uint8Array object to process the binary data acquired from an XmlHttpRequest:

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Uint8Array(buffer.byteLength);
             for (var i = 0; i < ints.length; i++) {
                 ints[i] = dataview.getUint8(i);
             }
         alert(ints[10]);
         }
     }
```

## Constants

The following table lists the constants of the **Uint8Array** object.

|Constant|Description|
|:-------|:----------|
|[BYTES\_PER\_ELEMENT Constant](/javascript/Uint8Array/BYTES_PER_ELEMENT)|The size in bytes of each element in the array.|

## Properties

The following table lists the constants of the **Uint8Array** object.

|Property|Description|
|:-------|:----------|
|[buffer Property](/javascript/Uint8Array/buffer)|Read-only. Gets the ArrayBuffer that is referenced by this array.|
|[byteLength Property](/javascript/Uint8Array/byteLength)|Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[byteOffset Property](/javascript/Uint8Array/byteOffset)|Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[length Property](/javascript/Uint8Array/length)|The length of the array.|

## Methods

The following table lists the methods of the **Uint8Array** object.

|Method|Description|
|:-----|:----------|
|[get Method](/javascript/Uint8Array/get)|Omittable. Gets the element at the specified index.|
|[set Method (Uint8Array)](/javascript/Uint8Array/set)|Sets a value or an array of values.|
|[subarray Method (Uint8Array)](/javascript/Uint8Array/subarray)|Gets a new Uint8Array view of the ArrayBuffer store for this array.|

