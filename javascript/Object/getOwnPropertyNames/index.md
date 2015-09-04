---
title: getOwnPropertyNames
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns the names of the own properties of an object. The own properties of an object are those that are defined directly on that object, and are not inherited from the object''s prototype. The properties of an object include both fields (objects) and functions.'
uri: javascript/Object/getOwnPropertyNames

---
# getOwnPropertyNames

## Summary

Returns the names of the own properties of an object. The own properties of an object are those that are defined directly on that object, and are not inherited from the object's prototype. The properties of an object include both fields (objects) and functions.

## Syntax

    Object.getOwnPropertyNames( object )

**object**
:   Required. The object that contains the own properties.

## Return Value

An array that contains the names of the own properties of the object.

## Examples

The following example creates an object that has three properties and a method. It then uses the **getOwnPropertyNames** method to obtain the own properties (including the method) of the object.

``` {.js}
function Pasta(grain, width, shape) {
     // Define properties.
     this.grain = grain;
     this.width = width;
     this.shape = shape;
     this.toString = function () {
         return (this.grain + ", " + this.width + ", " + this.shape);
     }
 }

 // Create an object.
 var spaghetti = new Pasta("wheat", 0.2, "circle");

 // Get the own property names.
 var arr = Object.getOwnPropertyNames(spaghetti);
 document.write (arr);

 // Output:
 //   grain,width,shape,toString
```

The following example displays the names of properties that start with the letter 's' in a spaghetti object constructed with the Pasta constructor.

``` {.js}
function Pasta(grain, size, shape) {
     this.grain = grain;
     this.size = size;
     this.shape = shape;
 }

 var spaghetti = new Pasta("wheat", 2, "circle");

 var names = Object.getOwnPropertyNames(spaghetti).filter(CheckKey);
 document.write(names);

 // Check whether the first character of a string is 's'.
 function CheckKey(value) {
     var firstChar = value.substr(0, 1);
     if (firstChar.toLowerCase() == 's')
         return true;
     else
          return false;
 }
 // Output:
 // size,shape
```

## Remarks

The **getOwnPropertyNames** method returns the names of both enumerable and non-enumerable properties and methods. To return only the names of enumerable properties and methods, you can use the [Object.keys Function](/javascript/Object/keys).

## Exceptions

If the value supplied for the object argument is not the name of an object, a TypeError exception is thrown.

## See also

### Other articles

-   [Object.keys Function](/javascript/Object/keys)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff688126(v=vs.94).aspx)

