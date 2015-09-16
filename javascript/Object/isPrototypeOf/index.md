---
title: 'isPrototypeOf'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/bch72c9e(v=vs.94).aspx)'
compatibility:
  feature: isPrototypeOf
  topic: javascript
readiness: 'Ready to Use'
summary: 'Determines whether an object exists in another object''s prototype chain.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Object/isPrototypeOf

---
## Summary

Determines whether an object exists in another object's prototype chain.

## Syntax

    isPrototypeOf( object2 )

**object2**
:   Required. Another object whose prototype chain is to be checked.

## Examples

The following example illustrates the use of the **isPrototypeOf** method.

``` js
var re = new RegExp();
 document.write(RegExp.prototype.isPrototypeOf(re));

 // Output: true
```

## Remarks

The **isPrototypeOf** method returns true if object2 has object1 in its prototype chain. The prototype chain is used to share functionality between instances of the same object type. The **isPrototypeOf** method returns false when object2 is not an object or when object1 does not appear in the prototype chain of the object2.

## See also

### Specification

[15.2.4.6 Object.prototype.isPrototypeOf (V)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.2.4.6) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

