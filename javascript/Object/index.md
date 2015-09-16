---
title: 'Object'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/kb6te8d3(v=vs.94).aspx)'
compatibility:
  feature: Object
  topic: javascript
readiness: 'Ready to Use'
summary: 'Provides functionality common to all JavaScript objects.'
tags:
  - JS
  - Basic
uri: javascript/Object

---
## Summary

Provides functionality common to all JavaScript objects.

## Syntax

    obj  = new Object( [ value ] )

**obj**
:   Required. The variable name to which the Object object is assigned.

**value**
:   Optional. Any one of the JavaScript primitive data types (Number, Boolean, or String). If value is an object, the object is returned unmodified. If value is null , **undefined** , or not supplied, an object with no content is created.

## Remarks

The Object object is contained in all other JavaScript objects; all of its methods and properties are available in all other objects. The methods can be redefined in user-defined objects, and are called by JavaScript at appropriate times. The **toString** method is an example of a frequently redefined Object method.

In this language reference, the description of each Object method includes both default and object-specific implementation information for the intrinsic JavaScript objects.

## Properties

The following table lists properties of the **Object Object**.

|Property|Description|
|:-------|:----------|
|[constructor Property](/javascript/Object/constructor)|Specifies the function that creates an object.|
|[prototype Property](/javascript/Object/prototype)|Returns a reference to the prototype for a class of objects.|

## Functions

The following table lists functions of the **Object Object**.

|Function|Description|
|:-------|:----------|
|[Object.create Function](/javascript/Object/create)|Creates an object that has a specified prototype, and that optionally contains specified properties.|
|[Object.defineProperties Function](/javascript/Object/defineProperties)|Adds one or more properties to an object, and/or modifies attributes of existing properties.|
|[Object.defineProperty Function](/javascript/Object/defineProperty)|Adds a property to an object, or modifies attributes of an existing property.|
|[Object.freeze Function](/javascript/Object/freeze)|Prevents the modification of existing property attributes and values, and prevents the addition of new properties.|
|[Object.getOwnPropertyDescriptor Function](/javascript/Object/getOwnPropertyDescriptor)|Returns the definition of a data property or an accessor property.|
|[Object.getOwnPropertyNames Function](/javascript/Object/getOwnPropertyNames)|Returns the names of the properties and methods of an object.|
|[Object.getPrototypeOf Function](/javascript/Object/getPrototypeOf)|Returns the prototype of an object.|
|[Object.isExtensible Function](/javascript/Object/isExtensible)|Returns a value that indicates whether new properties can be added to an object.|
|[Object.isFrozen Function](/javascript/Object/isFrozen)|Returns true if existing property attributes and values cannot be modified in an object and new properties cannot be added to the object.|
|[Object.isSealed Function](/javascript/Object/isSealed)|Returns true if existing property attributes cannot be modified in an object and new properties cannot be added to the object.|
|[Object.keys Function](/javascript/Object/keys)|Returns the names of the enumerable properties and methods of an object.|
|[Object.preventExtensions Function](/javascript/Object/preventExtensions)|Prevents the addition of new properties to an object.|
|[Object.seal Function](/javascript/Object/seal)|Prevents the modification of attributes of existing properties, and prevents the addition of new properties.|

## Methods

The following table lists methods of the **Object Object**.

|Method|Description|
|:-----|:----------|
|[hasOwnProperty method](/javascript/Object/hasOwnProperty)|Returns a Boolean value that indicates whether an object has a property with the specified name.|
|[isPrototypeOf method](/javascript/Object/isPrototypeOf)|Returns a Boolean value that indicates whether an object exists in another object's prototype hierarchy.|
|[propertyIsEnumerable method](/javascript/Object/propertyIsEnumerable)|Returns a Boolean value that indicates whether a specified property is part of an object and whether it is enumerable.|
|[toLocaleString method](/javascript/Object/toLocaleString)|Returns an object converted to a string based on the current locale.|
|[toString method](/javascript/Object/toString)|Returns a string representation of an object.|
|[valueOf method](/javascript/Object/valueOf)|Returns the primitive value of the specified object.|

## See also

### Other articles

-   [JavaScript Objects](/javascript/objects)

