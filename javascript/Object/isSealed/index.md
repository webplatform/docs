---
title: isSealed
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff806189(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns true if existing property attributes cannot be modified in an object and new properties cannot be added to the object.'
tags:
  - JS
  - Basic
uri: javascript/Object/isSealed

---
## <span>Summary</span>

Returns true if existing property attributes cannot be modified in an object and new properties cannot be added to the object.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    Object.isSealed( object )

**object**
:   Required. The object to test.

## <span>Return Value</span>

true if both of the following are true:

-   The object is non-extensible, which indicates that new properties cannot be added to the object.
-   The configurable attribute is false for all existing properties.

If the object does not have any properties, the function returns true if the object is non-extensible.

## <span>Examples</span>

The following example illustrates the use of the **Object.isSealed** function.

``` js
// Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };

 // Seal the object, and verify that it is sealed.
 Object.seal(obj);
 document.write(Object.isSealed(obj));
 document.write("<br/>");

 // Try to add a new property, and then verify that it is not added.
 obj.newProp = 50;
 document.write(obj.newProp);
 document.write("<br/>");

 // Try to delete a property, and then verify that it is still present.
 delete obj.length;
 document.write(obj.length);

 // Output:
 // true
 // undefined
 // 10
```

## <span>Remarks</span>

When the configurable attribute of a property is false , the property attributes cannot be changed and the property cannot be deleted. When writable is false , the data property value cannot be changed. When configurable is false and writable is true , the value and writable attributes can be changed.

The **Object.isSealed** function does not use the writable attribute of properties to determine its return value.

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
|**Object.isSealed**|No|Yes|No|
|[Object.isFrozen](/javascript/Object/isFrozen)|No|Yes|Yes|

## <span>Exceptions</span>

If the object argument is not an object, a TypeError exception is thrown.

## <span>See also</span>

### <span>Other articles</span>

-   [Object.preventExtensions Function](/javascript/Object/preventExtensions)
-   [Object.seal Function](/javascript/Object/seal)
-   [Object.freeze Function](/javascript/Object/freeze)
-   [Object.isExtensible Function](/javascript/Object/isExtensible)
-   [Object.isFrozen Function](/javascript/Object/isFrozen)
-   [Object.defineProperty Function](/javascript/Object/defineProperty)
-   [Object.getOwnPropertyDescriptor Function](/javascript/Object/getOwnPropertyDescriptor)

