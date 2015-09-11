---
title: constructor
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155181(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Specifies the function that creates an Error.'
tags:
  - JS
  - Basic
uri: javascript/Error/constructor

---
## <span>Summary</span>

Specifies the function that creates an Error.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    error.constructor

## <span>Examples</span>

The following example illustrates the use of the constructor property.

``` js
var x = new Error("This is an error");

 if (x.constructor == Error)
     document.write("Object is an error.");

 // Output:
 // Object is an error.
```

## <span>Remarks</span>

The required error is the name of an error object.

The **constructor** property is a member of the prototype of every object that has a prototype. The **constructor** property contains a reference to the function that constructs instances of that particular object.

