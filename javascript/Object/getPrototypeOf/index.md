---
title: getPrototypeOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff877835(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the prototype of an object.'
tags:
  - JS
  - Basic
uri: javascript/Object/getPrototypeOf

---
## Summary

Returns the prototype of an object.

## Syntax

    Object.getPrototypeOf( object )

**object**
:   Required. The object that references the prototype.

## Return Value

The prototype of the object argument. The prototype is also an object.

## Examples

The following example illustrates the use of the **Object.getPrototypeOf** function.

``` js
// Create a constructor function.
 function Pasta(grain, width) {
     this.grain = grain;
     this.width = width;
 }
 // Create an object from the pasta constructor.
 var spaghetti = new Pasta("wheat", 0.2);

 // Obtain the prototype from the object.
 var proto = Object.getPrototypeOf(spaghetti);

 // Add a property to the prototype and validate that
 // the original object has the property.
 proto.foodgroup = "carbohydrates";
 document.write(spaghetti.foodgroup + " ");

 // Verify that the prototype obtained from the object
 // is the same as the prototype of the constructor.
 var result = (proto === Pasta.prototype);
 document.write(result + " ");

 // Verify that prototype obtained from the object
 // is a prototype of the original object.
 var result = proto.isPrototypeOf(spaghetti);
 document.write(result);

 // Output: carbohydrates true true
```

The following example uses the **Object.getPrototypeOf** function to validate data types.

``` js
var reg = /a/;
 var result = (Object.getPrototypeOf(reg) === RegExp.prototype);
 document.write(result + " ");

 var err = new Error("an error");
 var result = (Object.getPrototypeOf(err) === Error.prototype);
 document.write(result);

 // Output: true true
```

## Exceptions

If the object argument is not an object, a TypeError exception is thrown.

## See also

### Other articles

-   [prototype Property (Object)](/javascript/Object/prototype)
-   [isPrototypeOf Method (Object)](/javascript/Object/isPrototypeOf)

