---
title: 'isFrozen'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff806185(v=vs.94).aspx)'
compatibility:
  feature: isFrozen
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns true if existing property attributes and values cannot be modified in an object, and new properties cannot be added to the object.'
tags:
  - JS
  - Basic
uri: javascript/Object/isFrozen

---
## Summary

Returns true if existing property attributes and values cannot be modified in an object, and new properties cannot be added to the object.

## Syntax

    Object.isFrozen( object )

**object**
:   Required. The object to test.

## Return Value

true if all of the following are true:

-   The object is non-extensible, which indicates that new properties cannot be added to the object.
-   The configurable attribute is false for all existing properties.
-   The writable attribute is false for all existing data properties.

If the object has no existing properties, the function returns true if the object is non-extensible.

## Examples

The following example illustrates the use of the **Object.isFrozen** function.

``` js
// Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };

 // Freeze the object, and verify that it is frozen.
 Object.freeze(obj);
 document.write(obj.isFrozen());

 // Try to add a new property, and then verify that it is not added.
 obj.newProp = 50;
 document.write (obj.newProp);
 document.write ("<br/>");

 // Try to delete a property, and then verify that it is still present.
 delete obj.length;
 document.write (obj.length);
 document.write ("<br/> ");

 // Try to change a property value, and then verify that it is not changed.
 obj.pasta = "linguini";
 document.write (obj.pasta);

 // Output:
 // true
 // undefined
 // 10
 // spaghetti
```

## Remarks

When the configurable attribute of a property is false , the property attributes cannot be changed and the property cannot be deleted. When writable is false , the data property value cannot be changed. When configurable is false and writable is true , the value and writable attributes can be changed.

For information about how to set property attributes, see [Object.defineProperty Function](/javascript/Object/defineProperty). To obtain the attributes of a property, you can use the [Object.getOwnPropertyDescriptor Function](/javascript/Object/getOwnPropertyDescriptor).

The following related functions prevent the modification of object attributes.

|Function|Object is made non-extensible|configurable is set to false for each property|writable is set to false for each property|
|:-------|:----------------------------|:---------------------------------------------|:-----------------------------------------|
|[Object.preventExtensions](/javascript/Object/preventExtensions)|Yes|No|No|
|[Object.seal](/javascript/Object/seal)|Yes|Yes|No|
|[Object.freeze](/javascript/Object/freeze)|Yes|Yes|Yes|

The following functions return true if all of the conditions marked in the following table are true.

|Function|Object is extensible?|configurable is false for all properties?|writable is false for all data properties?|
|:-------|:--------------------|:----------------------------------------|:-----------------------------------------|
|[Object.isExtensible](/javascript/Object/isExtensible)|Yes|No|No|
|[Object.isSealed](/javascript/Object/isSealed)|No|Yes|No|
|**Object.isFrozen**|No|Yes|Yes|

## Exceptions

If the object argument is not an object, a TypeError exception is thrown.

## See also

### Other articles

-   [Object.preventExtensions Function](/javascript/Object/preventExtensions)
-   [Object.seal Function](/javascript/Object/seal)
-   [Object.freeze Function](/javascript/Object/freeze)
-   [Object.isExtensible Function](/javascript/Object/isExtensible)
-   [Object.isSealed Function](/javascript/Object/isSealed)
-   [Object.defineProperty Function](/javascript/Object/defineProperty)
-   [Object.getOwnPropertyDescriptor Function](/javascript/Object/getOwnPropertyDescriptor)
-   [Object.getOwnPropertyNames Function](/javascript/Object/getOwnPropertyNames)

