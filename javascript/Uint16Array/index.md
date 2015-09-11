---
title: Uint16Array
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212484(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'A typed array of 16-bit unsigned integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.'
tags:
  - JS
  - Basic
uri: javascript/Uint16Array

---
## <span>Summary</span>

A typed array of 16-bit unsigned integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    uint16Array = new Uint16Array( length );

<span class="language">JavaScript</span>

    uint16Array = new Uint16Array( array );

<span class="language">JavaScript</span>

    uint16Array = new Uint16Array( buffer , byteOffset , length );

**uint16Array**
:   Required. The variable name to which the **Uint16Array** object is assigned.

**length**
:   Specifies the length (in bytes) of the array.

**array**
:   The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Uint16 type.

**buffer**
:   The ArrayBuffer that the Uint16Array represents.

**byteOffset**
:   Optional. Specifies the offset in bytes from the start of the buffer at which the Uint16Array should begin.

**length**
:   The length of the array.

## <span>Examples</span>

The following example shows how to use a Uint16Array object to process the binary data acquired from an XmlHttpRequest:

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Uint16Array(buffer.byteLength / 2);
             for (var i = 0; i < ints.length; i++) {
                 ints[i] = dataview.getUint16(i * 2);
             }
         alert(ints[10]);
         }
     }
```

## <span>Constants</span>

The following table lists the constants of the **Uint16Array** object.

|Constant|Description|
|:-------|:----------|
|[BYTES\_PER\_ELEMENT Constant](/javascript/Uint16Array/BYTES_PER_ELEMENT)|The size in bytes of each element in the array.|

## <span>Properties</span>

The following table lists the constants of the **Uint16Array** object.

|Property|Description|
|:-------|:----------|
|[buffer Property](/javascript/Uint16Array/buffer)|Read-only. Gets the ArrayBuffer that is referenced by this array.|
|[byteLength Property](/javascript/Uint16Array/byteLength)|Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[byteOffset Property](/javascript/Uint16Array/byteOffset)|Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.|
|[length Property](/javascript/Uint16Array/length)|The length of the array.|

## <span>Methods</span>

The following table lists the methods of the **Uint16Array** object.

|Method|Description|
|:-----|:----------|
|[get Method](/javascript/Uint16Array/get)|Omittable. Gets the element at the specified index.|
|[set Method (Uint16Array)](/javascript/Uint16Array/set)|Sets a value or an array of values.|
|[subarray Method (Uint16Array)](/javascript/Uint16Array/subarray)|Gets a new Uint16Array view of the ArrayBuffer store for this array.|

