---
title: set
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212906(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets a value or an array of values.'
tags:
  - JS
  - Basic
uri: javascript/Float32Array/set

---
## Summary

Sets a value or an array of values.

## Syntax

    int8Array.set(index, value);

    int8Array.set(array, offset);

**index**
:   The index of the location to set.

**value**
:   The value to set.

**array**
:   A typed or untyped array of values to set.

**offset**
:   The index in the current array at which the values are to be written.

## Examples

The following example shows how to set the first element of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var floatArr = new Float32Array(buffer.byteLength / 4);
             floatArr.set(0, 9);
         }
     }
```

## Remarks

If the input array is a TypedArray, the two arrays may use the same underlying ArrayBuffer. In this situation, setting the values takes place as if all the data is first copied into a temporary buffer that does not overlap either of the arrays, and then the data from the temporary buffer is copied into the current array.

If the offset plus the length of the given array is out of range for the current TypedArray, an exception is raised.

