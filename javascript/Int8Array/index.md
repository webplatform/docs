---
title: Int8Array
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212462(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'A typed array of 8-bit integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.'
tags:
  - JS
  - Basic
uri: javascript/Int8Array

---
## <span>Summary</span>

A typed array of 8-bit integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    int8Array = new Int8Array( length );

<span class="language">JavaScript</span>

    intArray = new IntArray( array );

<span class="language">JavaScript</span>

    intArray = new IntArray( buffer , byteOffset , length );

**int8Array**
:   Required. The variable name to which the **Int8Array** object is assigned.

**length**
:   Specifies the length (in bytes) of the array.

**array**
:   The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Int8 type.

**buffer**
:   The ArrayBuffer that the Int8Array represents.

**byteOffset**
:   Optional. Specifies the offset in bytes from the start of the buffer at which the Int8Array should begin.

**length**
:   The length of the array.

## <span>Examples</span>

The following example shows how to use an Int8Array object to process the binary data acquired from an XmlHttpRequest:

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Int8Array(buffer.byteLength);
             for (var i = 0; i < ints.length; i++) {
                 ints[i] = dataview.getInt8(i);
             }
         alert(ints[10]);
         }
     }
```

## <span>Constants</span>

The following table lists the constants of the **Int8Array** object.

|Constant|Description|
|:-------|:----------|
|[BYTES\_PER\_ELEMENT Constant](/javascript/Int8Array/BYTES_PER_ELEMENT)|The size in bytes of each element in the array.|

## <span>Properties</span>

The following table lists the constants of the **Int8Array** object.

|Property|Description|
|:-------|:----------|
|[buffer Property](/javascript/Int8Array/buffer)|Read-only. Gets the ArrayBuffer that is referenced by this array.|
|[byteLength Property](/javascript/Int8Array/byteLength)|Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[byteOffset Property](/javascript/Int8Array/byteOffset)|Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[length Property](/javascript/Int8Array/length)|The length of the array.|

## <span>Methods</span>

The following table lists the methods of the **Int8Array** object.

|Method|Description|
|:-----|:----------|
|[get Method](/javascript/Int8Array/get)|Omittable. Gets the element at the specified index.|
|[set Method (Int8Array)](/javascript/Int8Array/set)|Sets a value or an array of values.|
|[subarray Method (Float64Array)](/javascript/Float64Array/subarray)|Gets a new Int8Array view of the ArrayBuffer store for this array.|

