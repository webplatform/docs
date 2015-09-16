---
title: hasOwnProperty
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/328kyd6z(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Determines whether an object has a property with the specified name.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Object/hasOwnProperty

---
## Summary

Determines whether an object has a property with the specified name.

## Syntax

    hasOwnProperty( proName )

**proName**
:   Required. String value of a property name.

## Examples

In the following example, all String objects share a common split method. The following code will display **false** and **true**.

``` js
var s = new String("Sample");
 document.write(s.hasOwnProperty("split"));
 document.write("<br/>");
 document.write(String.prototype.hasOwnProperty("split"));

 // Output:
 // false
 // true
```

## Remarks

The **hasOwnProperty** method returns true if object has a property of the specified name, false if it does not. This method does not check the properties in the object's prototype chain; the property must be a member of the object itself.

## See also

### Specification

[15.2.4.5 Object.prototype.hasOwnProperty (V)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.2.4.5) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

