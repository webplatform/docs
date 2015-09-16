---
title: constructor
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj159602(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Specifies the function that creates a Number.'
tags:
  - JS
  - Basic
uri: javascript/Number/constructor

---
## Summary

Specifies the function that creates a Number.

## Syntax

<span class="language">JavaScript</span>

    number.constructor

## Examples

The following example illustrates the use of the constructor property.

``` js
var num = new Number();

 if (num.constructor == Number)
     document.write("Object is a Number.");
 else
     document.write("Object is not a Number.");

 // Output:
 // Object is a Number.
```

## Remarks

The required number is the name of a string.

The **constructor** property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the **Global** and **Math** objects. The **constructor** property contains a reference to the function that constructs instances of that particular object.

