---
title: 'constructor'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/c1hcx253(v=vs.94).aspx)'
compatibility:
  feature: constructor
  topic: javascript
readiness: 'Ready to Use'
summary: 'Specifies the function that creates an object.'
tags:
  - JS
  - Basic
uri: javascript/Object/constructor

---
## Summary

Specifies the function that creates an object.

## Syntax

    object.constructor

## Examples

The following example illustrates the use of the constructor property.

``` js
// A constructor function.
 function MyObj() {
     this.number = 1;
 }

 var x = new String("Hi");

 if (x.constructor == String)
     document.write("Object is a String.");
 document.write ("<br />");

 var y = new MyObj;
 if (y.constructor == MyObj)
     document.write("Object constructor is MyObj.");

 // Output:
 // Object is a String.
 // Object constructor is MyObj.
```

## Remarks

The required object is the name of an object or function.

The **constructor** property is a member of the prototype of every object that has a prototype. This includes all intrinsic JavaScript objects except the **Global** and **Math** objects. The **constructor** property contains a reference to the function that constructs instances of that particular object.

## See also

### Other articles

-   [prototype Property (Object)](/javascript/Object/prototype)

