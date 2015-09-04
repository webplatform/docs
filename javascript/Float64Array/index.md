---
title: Float64Array
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'A typed array of 64-bit float values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.'
uri: javascript/Float64Array

---
# Float64Array

## Summary

A typed array of 64-bit float values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

## Syntax

    float64Array = new Float64Array( length );

    float64Array = new Float64Array( array );

    float64Array = new Float64Array( buffer , byteOffset , length );

**float64Array**
:   Required. The variable name to which the **Float64Array** object is assigned.

**length**
:   Specifies the length (in bytes) of the array.

**array**
:   The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Float64 type.

**buffer**
:   The ArrayBuffer that the Float64Array represents.

**byteOffset**
:   Optional. Specifies the offset in bytes from the start of the buffer at which the Float64Array should begin.

**length**
:   The length of the array.

## Examples

The following example shows how to use a Float64Array object to process the binary data acquired from an XmlHttpRequest:

``` {.js}
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Float64Array(buffer.byteLength / 8);
             for (var i = 0; i < ints.length; i++) {
                 ints[i] = dataview.getFloat64(i * 8);
             }
         alert(ints[10]);
         }
     }
```

## Constants

The following table lists the constants of the **Float64Array** object.

Constant
:   Description
[BYTES\_PER\_ELEMENT Constant](/javascript/Float64Array/BYTES_PER_ELEMENT)
:   The size in bytes of each element in the array.

## Properties

The following table lists the constants of the **Float64Array** object.

Property
:   Description
[buffer Property](/javascript/Float64Array/byteLength)
:   Read-only. Gets the ArrayBuffer that is referenced by this array.
[byteLength Property](/javascript/Float64Array/byteLength)
:   Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
[byteOffset Property](/javascript/Float64Array/length)
:   Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
[length Property](/javascript/Float64Array/length)
:   The length of the array.

## Methods

The following table lists the methods of the **Float64Array** object.

Method
:   Description
[get Method](/javascript/Float64Array/get)
:   Omittable. Gets the element at the specified index.
[set Method (Float64Array)](/javascript/Float64Array/set)
:   Sets a value or an array of values.
[subarray Method (Float64Array)](/javascript/Float64Array/subarray)
:   Gets a new Float64Array view of the ArrayBuffer store for this array.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212931(v=vs.94).aspx)

