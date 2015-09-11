---
title: getOwnPropertyDescriptor
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dd548686(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the own property descriptor of the specified object. An own property descriptor is one that is defined directly on the object and is not inherited from the object''s prototype.'
tags:
  - JS
  - Basic
uri: javascript/Object/getOwnPropertyDescriptor

---
## <span>Summary</span>

Gets the own property descriptor of the specified object. An own property descriptor is one that is defined directly on the object and is not inherited from the object's prototype.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    Object.getOwnPropertyDescriptor( object , propertyname )

**object**
:   Required. The object that contains the property.

**propertyname**
:   Required. The name of the property.

## <span>Return Value</span>

The descriptor of the property.

## <span>Examples</span>

The following example gets a data property descriptor and uses it to make the property read-only.

``` js
// Create a user-defined object.
var obj = {};

// Add a data property.
obj.newDataProperty = "abc";

// Get the property descriptor.
var descriptor = Object.getOwnPropertyDescriptor(obj, "newDataProperty");

// Change a property attribute.
descriptor.writable = false;
Object.defineProperty(obj, "newDataProperty", descriptor);
```

To list the property attributes, you can add the following code to this example.

``` js
// Get the descriptor from the object.
var desc2 = Object.getOwnPropertyDescriptor(obj, "newDataProperty");

// List the descriptor attributes.
for (var prop in desc2) {
    document.write(prop + ': ' + desc2[prop]);
    document.write("<br />");
}

// Output:
// value: abc
// writable: false
// enumerable: true
// configurable: true
```

## <span>Remarks</span>

You can use the **Object.getOwnPropertyDescriptor** function to obtain a descriptor object that describes attributes of the property.

The [Object.defineProperty Function](/javascript/Object/defineProperty) is used to add or modify properties.

## <span>See also</span>

### <span>Other articles</span>

-   [Object.defineProperty Function](/javascript/Object/defineProperty)

