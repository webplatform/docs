---
title: constructor
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Specifies the function that creates an Error.'
uri: javascript/Error/constructor

---
# constructor

## Summary

Specifies the function that creates an Error.

## Syntax

    error.constructor

## Examples

The following example illustrates the use of the constructor property.

``` {.js}
var x = new Error("This is an error");

 if (x.constructor == Error)
     document.write("Object is an error.");

 // Output:
 // Object is an error.
```

## Remarks

The required error is the name of an error object.

The **constructor** property is a member of the prototype of every object that has a prototype. The **constructor** property contains a reference to the function that constructs instances of that particular object.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155181(v=vs.94).aspx)

