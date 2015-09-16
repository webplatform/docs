---
title: isExtensible
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff806188(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a value that indicates whether new properties can be added to an object.'
tags:
  - JS
  - Basic
uri: javascript/Object/isExtensible

---
## Summary

Returns a value that indicates whether new properties can be added to an object.

## Syntax

<span class="language">JavaScript</span>

    Object.isExtensible( object )

**object**
:   Required. The object to test.

## Return Value

true if the object is extensible, which indicates that new properties can be added to the object; otherwise, false.

## Examples

The following example illustrates the use of the **Object.isExtensible** function.

``` js
// Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };

 // Make the object non-extensible.
 Object.preventExtensions(obj);

 // Try to add a new property, and then verify that it is not added.
 obj.newProp = 50;
 document.write(obj.newProp);

 // Output:
 undefined
```

## Remarks

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
|**Object.isExtensible**|Yes|No|No|
|[Object.isSealed](/javascript/Object/isSealed)|No|Yes|No|
|[Object.isFrozen](/javascript/Object/isFrozen)|No|Yes|Yes|

## Exceptions

If the object argument is not an object, a TypeError exception is thrown.

## See also

### Other articles

-   [Object.preventExtensions Function](/javascript/Object/preventExtensions)
-   [Object.seal Function](/javascript/Object/seal)
-   [Object.freeze Function](/javascript/Object/freeze)
-   [Object.isSealed Function](/javascript/Object/isSealed)
-   [Object.isFrozen Function](/javascript/Object/isFrozen)

