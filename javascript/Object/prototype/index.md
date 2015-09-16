---
title: prototype
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/f5s9ycex(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a reference to the prototype for a class of objects.'
tags:
  - JS
  - Basic
uri: javascript/Object/prototype

---
## Summary

Returns a reference to the prototype for a class of objects.

## Syntax

<span class="language">JavaScript</span>

    objectName.prototype

## Examples

The objectName argument is the name of an object.

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

 // Output:
 // 25
```

## Remarks

All intrinsic JavaScript objects have a **prototype** property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

The method and property lists for each intrinsic object in this language reference indicate which ones are part of the object's prototype, and which are not.

## See also

### Other articles

-   [constructor Property (Object)](/javascript/Object/constructor)

