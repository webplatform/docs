---
title: 'defineProperties'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff800817(v=vs.94).aspx)'
compatibility:
  feature: defineProperties
  topic: javascript
readiness: 'Ready to Use'
summary: 'Adds one or more properties to an object, and/or modifies attributes of existing properties.'
tags:
  - JS_Basic
uri: javascript/Object/defineProperties

---
## Summary

Adds one or more properties to an object, and/or modifies attributes of existing properties.

## Syntax

    object.defineProperties( object , descriptors )

**object**
:   Required. The object on which to add or modify the properties. This can be a native JavaScript object or a DOM object.

**descriptors**
:   Required. A JavaScript object that contains one or more descriptor objects. Each descriptor object describes a data property or an accessor property.

## Return Value

The object that was passed to the function.

## Examples

**Adding Properties**

In the following example, the **Object.defineProperties** function adds a data property and an accessor property to a user-defined object.

The example uses an object literal to create the descriptors object with the `newDataProperty` and `newAccessorProperty` descriptor objects.

``` js
var newLine = "<br />";

var obj = {};
Object.defineProperties(obj, {
    newDataProperty: {
        value: 101,
        writable: true,
        enumerable: true,
        configurable: true
    },
    newAccessorProperty: {
        set: function (x) {
            document.write("in property set accessor" + newLine);
            this.newaccpropvalue = x;
        },
        get: function () {
            document.write("in property get accessor" + newLine);
            return this.newaccpropvalue;
        },
        enumerable: true,
        configurable: true
    });

// Set the accessor property value.
obj.newAccessorProperty = 10;
document.write ("newAccessorProperty value: " + obj.newAccessorProperty + newLine);

// Output:
// in property set accessor
// in property get accessor
// newAccessorProperty value: 10
```

Like the previous example, the following example adds properties dynamically instead of with an object literal.

``` js
var newLine = "<br />";

// Create the descriptors object.
var descriptors = new Object();

// Add a data property descriptor to the descriptors object.
descriptors.newDataProperty = new Object();
descriptors.newDataProperty.value = 101;
descriptors.newDataProperty.writable = true;
descriptors.newDataProperty.enumerable = true;
descriptors.newDataProperty.configurable = true;

// Add an accessor property descriptor to the descriptors object.
descriptors.newAccessorProperty = new Object();
descriptors.newAccessorProperty.set = function (x) {
    document.write("in property set accessor" + newLine);
    this.newaccpropvalue = x;
};
descriptors.newAccessorProperty.get = function () {
    document.write("in property get accessor" + newLine);
    return this.newaccpropvalue;
};
descriptors.newAccessorProperty.enumerable = true;
descriptors.newAccessorProperty.configurable = true;

// Call the Object.defineProperties function.
var obj = new Object();
Object.defineProperties(obj, descriptors);

// Set the accessor property value.
obj.newAccessorProperty = 10;
document.write ("newAccessorProperty value: " + obj.newAccessorProperty + newLine);

// Output:
// in property set accessor
// in property get accessor
// newAccessorProperty value: 10
```

**Modifying Properties**

To modify property attributes for the object, add the following code. The **Object.defineProperties** function modifies the writable attribute of `newDataProperty` , and modifies the enumerable attribute of `newAccessorProperty`. It adds `anotherDataProperty` to the object because that property name does not already exist.

``` js
Object.defineProperties(obj, {
        newDataProperty: { writable: false },
        newAccessorProperty: { enumerable: false },
        anotherDataProperty: { value: "abc" }
    });
```

## Remarks

The descriptors argument is an object that contains one or more descriptor objects.

A data property is a property that can store and retrieve a value. A data property descriptor contains a value attribute, a writable attribute, or both. For more information, see Data Properties and Accessor Properties.

An accessor property calls a user-provided function every time the property value is set or retrieved. An accessor property descriptor contains a set attribute, a get attribute, or both.

If the object already has a property that has the specified name, the property attributes are modified. For more information, see [Object.defineProperty Function](/javascript/Object/defineProperty).

To create an object and add properties to the new object, you can use the [Object.create Function](/javascript/Object/create).

## See also

### Other articles

-   [Object.getOwnPropertyDescriptor Function](/javascript/Object/getOwnPropertyDescriptor)
-   [Object.getOwnPropertyNames Function](/javascript/Object/getOwnPropertyNames)
-   [Object.defineProperty Function](/javascript/Object/defineProperty)
-   [Object.create Function](/javascript/Object/create)
-   [Object Object](/javascript/Object)

