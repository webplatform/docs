---
title: 'constructor'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155291(v=vs.94).aspx)'
code_samples:
  - 'http://code.webplatform.org/gist/9237139'
compatibility:
  feature: constructor
  topic: javascript
readiness: 'Ready to Use'
summary: 'References the function which created the instance of the Array object.'
tags:
  - JS_Basic
  - JS_Property
uri: javascript/Array/constructor

---
## Summary

References the function which created the instance of the Array object.

## Syntax

    arrayObj.constructor

## Return Value

The function object which constructed the Array instance.

## Examples

The following example illustrates the use of the constructor property.

``` js
var x = new Array();

 if (x.constructor == Array)
     document.write("Object is an Array.");
 else
     document.write("Object is not an Array.");

 // Output:
 // Object is an Array.
```

[View live example](http://code.webplatform.org/gist/9237139)

## Remarks

The **constructor** property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the **Global** and **Math** objects. If the JavaScript interpreter falls back to their prototype object, the **constructor** property references the native `Object.prototype.constructor`.

    var my_obj = Math;
    document.write(my_obj.constructor === Math);

    // Output: false

The **constructor** property is only read-only for primitive values such as 1, true and "test".

    var my_obj = new Number(100);
    my_obj.constructor = String; // overwritten
    document.write(my_obj.constructor);

    // Output: function String() { [native code] }

    my_obj = 100;
    my_obj.constructor = String; // can't be overwritten
    document.write(my_obj.constructor);

    // Output: function Number() { [native code] }

## See also

### External resources

-   [JavaScript, by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
-   [Object.prototype.constructor, by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/constructor)

### Specification

-   [4.3.4 constructor](http://www.ecma-international.org/ecma-262/5.1/#sec-4.3.4)
-   [15.2.4.1 Object.prototype.constructor](http://www.ecma-international.org/ecma-262/5.1/#sec-15.2.4.1)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

