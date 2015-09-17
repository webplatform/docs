---
title: 'preventExtensions'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff806191(v=vs.94).aspx)'
compatibility:
  feature: preventExtensions
  topic: javascript
readiness: 'Ready to Use'
summary: 'Prevents the addition of new properties to an object.'
tags:
  - JS_Basic
uri: javascript/Object/preventExtensions

---
## Summary

Prevents the addition of new properties to an object.

## Syntax

    Object.preventExtensions( object )

**object**
:   Required. The object to make non-extensible.

## Return Value

The object that is passed to the function.

## Examples

The following example illustrates the use of the **Object.preventExtensions** function.

``` js
// Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };

 // Make the object non-extensible.
 Object.preventExtensions(obj);
 document.write(Object.isExtensible(obj));
 document.write("<br/>");

 // Try to add a new property, and then verify that it is not added.
 obj.newProp = 50;
 document.write(obj.newProp);

 // Output:
 // false
 // undefined
```

## Remarks

The **Object.preventExtensions** function makes an object non-extensible, so that new named properties cannot be added to it. After an object is made non-extensible, it cannot be made extensible.

For information about how to set property attributes, see [Object.defineProperty Function](/javascript/Object/defineProperty).

The following related functions prevent the modification of object attributes.

|Function|Object is made non-extensible|configurable is set to false for each property|writable is set to false for each property|
|:-------|:----------------------------|:---------------------------------------------|:-----------------------------------------|
|**Object.preventExtensions**|Yes|No|No|
|[Object.seal](/javascript/Object/seal)|Yes|Yes|No|
|[Object.freeze](/javascript/Object/freeze)|Yes|Yes|Yes|

The following functions return true if all of the conditions marked in the following table are true.

|Function|Object is extensible?|configurable is false for all properties?|writable is false for all data properties?|
|:-------|:--------------------|:----------------------------------------|:-----------------------------------------|
|[Object.isExtensible](/javascript/Object/isExtensible)|Yes|No|No|
|[Object.isSealed](/javascript/Object/isSealed)|No|Yes|No|
|[Object.isFrozen](/javascript/Object/isFrozen)|No|Yes|Yes|

## Exceptions

If the object argument is not an object, a TypeError exception is thrown.

## See also

### Other articles

-   [Object.seal Function](/javascript/Object/seal)
-   [Object.freeze Function](/javascript/Object/freeze)
-   [Object.isExtensible Function](/javascript/Object/isExtensible)
-   [Object.isSealed Function](/javascript/Object/isSealed)
-   [Object.isFrozen Function](/javascript/Object/isFrozen)

