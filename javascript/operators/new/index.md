---
title: 'new'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ec3z6dcc(v=vs.94).aspx)'
compatibility:
  feature: new
  topic: javascript
readiness: 'Ready to Use'
summary: 'Creates a new object.'
tags:
  - JS
  - Basic
uri: javascript/operators/new

---
## Summary

Creates a new object.

## Syntax

    new constructor ([ arguments ])

**constructor**
:   Required. The constructor of the object. The parentheses can be omitted if the constructor takes no arguments.

**arguments**
:   Optional. Any arguments to be passed to the new object's constructor.

## Examples

These are examples of valid uses of the **new** operator.

``` js
my_object = new Object;
my_array = new Array();
my_date = new Date("Jan 5 1996");
```

## Remarks

The new operator performs the following tasks:

-   It creates an object with no members.
-   It calls the constructor for that object, passing a pointer to the newly created object as the this pointer.
-   The constructor then initializes the object according to the arguments passed to the constructor.

## See also

### Other articles

-   [function Statement](/javascript/statements/function)

