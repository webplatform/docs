---
title: in
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Tests for the existence of a property in an object.'
uri: javascript/operators/in

---
# in

## Summary

Tests for the existence of a property in an object.

## Syntax

    result = property in object

**result**
:   Required. Any variable.

**property**
:   Required. An expression that evaluates to a string expression.

**object**
:   Required. Any object.

## Examples

The following example shows how to use the **in** operator:

``` {.js}
// Create an object that has some properties.
 var myObject = new Object();
 myObject.name = "James";
 myObject.age = "22";
 myObject.phone = "555 0234";

 if ("phone" in myObject)
    document.write ("property is present");
 else
    document.write ("property is not present");

 // Output: property is present
```

## Remarks

The **in** operator determines whether an object has a property named property. It also determines whether the property is part of the object's prototype chain. For more information about object prototypes, see Prototypes and Prototype Inheritance.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9k25hbz2(v=vs.94).aspx)

