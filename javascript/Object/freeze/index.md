---
title: freeze
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff806186(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Prevents the modification of existing property attributes and values, and prevents the addition of new properties.'
tags:
  - JS
  - Basic
uri: javascript/Object/freeze

---
## Summary

Prevents the modification of existing property attributes and values, and prevents the addition of new properties.

## Syntax

    Object.freeze( object )

**object**
:   Required. The object on which to lock the attributes.

## Return Value

The object that is passed to the function.

## Examples

The following example illustrates the use of the **Object.freeze** function.

``` js
// Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };

 // Freeze the object.
 Object.freeze(obj);

 // Try to add a new property, and then verify that it is not added.
     obj.newProp = 50;
     document.write(obj.newProp);
     document.write("<br/>");

 // Try to delete a property, and then verify that it is still present.
 delete obj.length;
 document.write(obj.length);
 document.write("<br/>");

 // Try to change a property value, and then verify that it is not changed.
 obj.pasta = "linguini";
 document.write(obj.pasta);

 // Output:
 // undefined
 // 10
 // spaghetti
```

## Remarks

The Object.freeze function does the following:

-   Makes the object non-extensible, so that new properties cannot be added to it.
-   Sets the configurable attribute to false for all properties of the object. When configurable is false , the property attributes cannot be changed and the property cannot be deleted.
-   Sets the writable attribute to false for all data properties of the object. When writable is false, the data property value cannot be changed.

For more information about how to set property attributes, see [Object.defineProperty Function](/javascript/Object/defineProperty). To obtain the attributes of a property, you can use the [Object.getOwnPropertyDescriptor Function](/javascript/Object/getOwnPropertyDescriptor).

The following related functions prevent the modification of object attributes.

|Function|Object is made non-extensible|configurable is set to false for each property|writable is set to false for each property|
|:-------|:----------------------------|:---------------------------------------------|:-----------------------------------------|
|[Object.preventExtensions](/javascript/Object/preventExtensions)|Yes|No|No|
|[Object.seal](/javascript/Object/seal)|Yes|Yes|No|
|**Object.freeze**|Yes|Yes|Yes|

The following functions return true if all of the conditions marked in the following table are true.

|Function|Object is extensible?|configurable is false for all properties?|writable is false for all data properties?|
|:-------|:--------------------|:----------------------------------------|:-----------------------------------------|
|[Object.isExtensible](/javascript/Object/isExtensible)|Yes|No|No|
|[Object.isSealed](/javascript/Object/isSealed)|No|Yes|Yes|
|[Object.isFrozen](/javascript/Object/isFrozen)|No|Yes|Yes|

## Exceptions

If the object argument is not an object, a TypeError exception is thrown.

## See also

### Other articles

-   [Object.preventExtensions Function](/javascript/Object/preventExtensions)
-   [Object.seal Function](/javascript/Object/seal)
-   [Object.isExtensible Function](/javascript/Object/isExtensible)
-   [Object.isSealed Function](/javascript/Object/isSealed)
-   [Object.isFrozen Function](/javascript/Object/isFrozen)

