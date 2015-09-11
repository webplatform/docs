---
title: propertyIsEnumerable
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/adebfyya(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Determines whether a specified property is enumerable.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Object/propertyIsEnumerable

---
## <span>Summary</span>

Determines whether a specified property is enumerable.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    propertyIsEnumerable( proName )

**proName**
:   Required. String value of a property name.

## <span>Examples</span>

``` js
var a = new Array("apple", "banana", "cactus");
 document.write(a.propertyIsEnumerable(1));

 // Output: true
```

## <span>Remarks</span>

The **propertyIsEnumerable** method returns true if proName exists in object and can be enumerated using a For loop. The **propertyIsEnumerable** method returns false if object does not have a property of the specified name or if the specified property is not enumerable. Typically, predefined properties are not enumerable, but user-defined properties are always enumerable.

The **propertyIsEnumerable** method does not consider objects in the prototype chain.

## <span>See also</span>

### <span>Specification</span>

[15.2.4.7 Object.prototype.propertyIsEnumerable (V)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.2.4.7) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

