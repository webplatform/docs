---
title: prototype
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns a reference to the prototype for an error.'
uri: javascript/Error/prototype

---
# prototype

## Summary

Returns a reference to the prototype for an error.

## Syntax

    error.prototype

## Examples

For example, to add a method to the **Error** object that returns the value of the largest element of the array, declare the function, add it to **Error.prototype** , and then use it.

``` {.js}
function getSeverity(){
     if (this.number > 1000)
         return "high";
     else
         return "low";
 }
 Error.prototype.getSev = getSeverity;
 var myError = new Error();
 myError.number = 5000;

 document.write(myError.getSev());

 // Output: high
```

## Remarks

The error argument is the name of an error.

Use the **prototype** property to provide a base set of functionality to an Error. New instances of an object "inherit" the behavior of the prototype assigned to that object.

All intrinsic JavaScript objects have a **prototype** property that is read-only. Properties and methods may be added to the prototype, but the object may not be assigned a different prototype. However, user-defined objects may be assigned a new prototype.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155286(v=vs.94).aspx)

