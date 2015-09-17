---
title: 'prototype'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj159612(v=vs.94).aspx)'
compatibility:
  feature: prototype
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns a reference to the prototype for a class of number.'
tags:
  - JS_Basic
uri: javascript/Number/prototype

---
## Summary

Returns a reference to the prototype for a class of number.

## Syntax

    number.prototype

## Examples

The number argument is the name of a number. Use the **prototype** property to provide a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object.

For example, to add a method to the **Number** object that returns the number of (integer) digits, declare the function, add it to **Number.prototype** , and then use it.

``` js
function number_digits() {
     var digits = 0;
     var num = this;
     while (num) >= 1) {
         digits++;
         num /= 10;
     }
     return digits;
 }

 Number.prototype.digits = number_digits;
 var myNumber = new Number(3456.789);
 document.write(myNumber.digits());
 // Output:
 // 4
```

## Remarks

All intrinsic JavaScript objects have a **prototype** property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

The method and property lists for each intrinsic object in this language reference indicate which ones are part of the object's prototype, and which are not.

