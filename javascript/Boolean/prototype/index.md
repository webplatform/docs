---
title: prototype
tags:
  0: JS
  1: Basic
  3: Property
readiness: 'Ready to Use'
summary: 'Returns a reference to the prototype for a Boolean.'
uri: javascript/Boolean/prototype

---
# prototype

## Summary

Returns a reference to the prototype for a Boolean.

## Syntax

    boolean.prototype

## Examples

Defines a function and then adds it to Boolean.prototype

``` {.js}
function isFalse( ){
     if (this.toString() == "false")
          return true;
     else
         return false;
 }
 Boolean.prototype.isFalse = isFalse;
 var bool = new Boolean(1);
 document.write(bool.isFalse());

 // Output:
 // false
```

Adds a function directly to the Boolean object through its prototype

``` {.js}
//Creates a toggle function for Boolean objects
// through its prototype. All new boolean objects will
// have this method.
Boolean.prototype.toggle = function (){
  return !this.valueOf();
}
```

## Remarks

The boolean argument is the name of an object.

The **prototype** property provides a base set of functionality to a class of objects. New instances of an object "inherit" the behavior of the prototype assigned to that object. Properties and methods may be added to the prototype, but builtin objects may not be assigned a different prototype.

For example, to add a method to the **Boolean** object that returns the value of the largest element of the array, declare the function, add it to **Boolean.prototype** , and then use it.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155296(v=vs.94).aspx)

