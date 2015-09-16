---
title: 'subarray'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212936(v=vs.94).aspx)'
compatibility:
  feature: subarray
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets a new Int16Array view of the ArrayBuffer Object store for this array, specifying the first and last members of the subarray.'
tags:
  - JS
  - Basic
uri: javascript/Int16Array/subarray

---
## Summary

Gets a new Int16Array view of the ArrayBuffer Object store for this array, specifying the first and last members of the subarray.

## Syntax

    var newInt16Array = int16Array.subarray(begin, end);

**newInt16Array**
:   The subarray returned by this method.

**begin**
:   The index of the beginning of the array.

**end**
:   The index of the end of the array.

## Examples

The following example shows how to get a subarray three elements long, starting with the first element of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var intArr = new Int16Array(buffer.byteLength / 2);
             var subArr = intArr.subarray(0, 2);
         }
     }
```

## Remarks

If either begin or end is negative, it refers to an index from the end of the array, as opposed to from the beginning. If end is unspecified, the subarray contains all elements from begin to the end of the typed array. The range specified by the begin and end values is clamped to the valid index range for the current array. If the computed length of the new typed array would be negative, it is clamped to zero. The returned array is of the same type as the array on which this method is invoked.

