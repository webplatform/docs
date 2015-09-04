---
title: constructor
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Specifies the function that creates a date.'
uri: javascript/Date/constructor

---
# constructor

## Summary

Specifies the function that creates a date.

## Syntax

    date.constructor

## Examples

The following example illustrates the use of the constructor property.

``` {.js}
var x = new Date("Hi");

 if (x.constructor == Date)
     document.write("Object is a date.");

 // Output:
 // Object is a date.
```

## Remarks

The required date is the name of a date object.

The **constructor** property is a member of the prototype of every object that has a prototype. The **constructor** property contains a reference to the function that constructs instances of that particular object.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155284(v=vs.94).aspx)

