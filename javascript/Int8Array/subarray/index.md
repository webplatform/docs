---
title: subarray
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212914(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets a new Int8Array view of the ArrayBuffer store for this array, referencing the elements at begin, inclusive, up to end, exclusive.'
tags:
  - JS
  - Basic
uri: javascript/Int8Array/subarray

---
## <span>Summary</span>

Gets a new Int8Array view of the ArrayBuffer store for this array, referencing the elements at begin, inclusive, up to end, exclusive.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var newInt8Array = int8Array.subset(begin, end);

**newInt8Array**
:   The subarray returned by this method.

**begin**
:   The index of the beginning of the array.

**end**
:   The index of the end of the array.

## <span>Examples</span>

The following example shows how to get a subarray three elements long, starting with the first element of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Int8Array(buffer.byteLength);
             var subArr = intArr.subarray(0, 2);
         }
     }
```

## <span>Remarks</span>

If either begin or end is negative, it refers to an index from the end of the array, as opposed to from the beginning. If end is unspecified, the subarray contains all elements from begin to the end of the TypedArray. The range specified by the begin and end values is clamped to the valid index range for the current array. If the computed length of the new TypedArray would be negative, it is clamped to zero. The returned TypedArray will be of the same type as the array on which this method is invoked.

