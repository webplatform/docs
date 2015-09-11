---
title: in
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9k25hbz2(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Tests for the existence of a property in an object.'
tags:
  - JS
  - Basic
uri: javascript/operators/in

---
## <span>Summary</span>

Tests for the existence of a property in an object.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    result = property in object

**result**
:   Required. Any variable.

**property**
:   Required. An expression that evaluates to a string expression.

**object**
:   Required. Any object.

## <span>Examples</span>

The following example shows how to use the **in** operator:

``` js
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

## <span>Remarks</span>

The **in** operator determines whether an object has a property named property. It also determines whether the property is part of the object's prototype chain. For more information about object prototypes, see Prototypes and Prototype Inheritance.

