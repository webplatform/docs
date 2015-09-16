---
title: 'delete'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/2b2z052x(v=vs.94).aspx)'
compatibility:
  feature: delete
  topic: javascript
readiness: 'Ready to Use'
summary: 'Deletes a property from an object, or removes an element from an array.'
tags:
  - JS
  - Basic
uri: javascript/operators/delete

---
## Summary

Deletes a property from an object, or removes an element from an array.

## Syntax

    delete expression

## Examples

The following example shows how to remove an element from an array.

``` js
// Create an array.
 var ar = new Array (10, 11, 12, 13, 14);

 // Remove an element from the array.
 delete ar[1];

 // Print the results.
 document.write ("element 1: " + ar[1]);
 document.write ("<br />");
 document.write ("array: " + ar);
 // Output:
 //  element 1: undefined
 //  array: 10,,12,13,14
```

The following example shows how to delete properties from an object.

``` js
// Create an object and add expando properties.
 var myObj = new Object();
 myObj.name = "Fred";
 myObj.count = 42;

 // Delete the properties from the object.
 delete myObj.name;
 delete myObj["count"];

 // Print the results.
 document.write ("name: " + myObj.name);
 document.write ("<br />");
 document.write ("count: " + myObj.count);
 // Output:
 //  name: undefined
 //  count: undefined
```

## Remarks

The expression argument is a valid JavaScript expression that usually results in a property name or array element.

If the result of expression is an object, the property specified in expression exists, and the object will not allow it to be deleted, false is returned.

In all other cases, true is returned.

