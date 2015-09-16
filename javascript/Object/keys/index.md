---
title: keys
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff688127(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the names of the enumerable properties and methods of an object.'
tags:
  - JS
  - Basic
uri: javascript/Object/keys

---
## Summary

Returns the names of the enumerable properties and methods of an object.

## Syntax

<span class="language">JavaScript</span>

    Object.keys( object )

**object**
:   Required. The object that contains the properties and methods. This can be an object that you created or an existing Document Object Model (DOM) object.

## Return Value

An array that contains the names of the enumerable properties and methods of the object.

## Examples

The following example creates an object that has three properties and a method. It then uses the **keys** method to get the properties and methods of the object.

``` js
// Create a constructor function.
 function Pasta(grain, width, shape) {
     this.grain = grain;
     this.width = width;
     this.shape = shape;

     // Define a method.
     this.toString = function () {
         return (this.grain + ", " + this.width + ", " + this.shape);
     }
 }

 // Create an object.
 var spaghetti = new Pasta("wheat", 0.2, "circle");

 // Put the enumerable properties and methods of the object in an array.
 var arr = Object.keys(spaghetti);
 document.write (arr);

 // Output:
 // grain,width,shape,toString
```

The following example displays the names of all enumerable properties that start with the letter "g" in the Pasta object.

``` js
// Create a constructor function.
 function Pasta(grain, width, shape) {
     this.grain = grain;
     this.width = width;
     this.shape = shape;
 }

 var polenta = new Pasta("corn", 1, "mush");

 var keys = Object.keys(polenta).filter(CheckKey);
 document.write(keys);

 // Check whether the first character of a string is "g".
 function CheckKey(value) {
     var firstChar = value.substr(0, 1);
     if (firstChar.toLowerCase() == "g")
         return true;
     else
         return false;
 }

 // Output:
 // grain
```

## Remarks

The **keys** method returns only the names of enumerable properties and methods. To return the names of both enumerable and non-enumerable properties and methods, you can use [Object.getOwnPropertyNames Function](/javascript/Object/getOwnPropertyNames).

For information about the enumerable attribute of a property, see [Object.defineProperty Function](/javascript/Object/defineProperty) and [Object.getOwnPropertyDescriptor Function](/javascript/Object/getOwnPropertyDescriptor).

## Exceptions

If the value supplied for the object argument is not the name of an object, a TypeError exception is thrown.

## See also

### Other articles

-   [Object.getOwnPropertyNames Function](/javascript/Object/getOwnPropertyNames)

