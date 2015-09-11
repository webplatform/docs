---
title: prototype
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155285(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a reference to the prototype for a class of array.'
tags:
  0: JS
  1: Basic
  3: Property
uri: javascript/Array/prototype

---
## <span>Summary</span>

Returns a reference to the prototype for a class of array.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    Array.prototype

## <span>Examples</span>

The array argument is the name of an array.

Use the **prototype** property to provide a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object.

For example, to add a method to the **Array** object that returns the value of the largest element of the array, declare the function, add it to **Array.prototype** , and then use it.

``` js
function array_max( ){
     var i, max = this[0];
     for (i = 1; i < this.length; i++)
     {
     if (max < this[i])
     max = this[i];
     }
     return max;
 }
 Array.prototype.max = array_max;
 var myArray = new Array(7, 1, 3, 11, 25, 9
 );
 document.write(myArray.max());

 // Output: 25
```

## <span>Remarks</span>

All intrinsic JavaScript objects have a **prototype** property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

The method and property lists for each intrinsic object in this language reference indicate which ones are part of the object's prototype, and which are not.

## <span>Requirements</span>

Supported in the following document modes: Quirks, Internet Explorer 6 standards, Internet Explorer 7 standards, Internet Explorer 8 standards, Internet Explorer 9 standards, Internet Explorer 10 standards, Internet Explorer 11 standards. Also supported in Windows Store apps. See Version Information.

