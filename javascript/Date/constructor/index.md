---
title: constructor
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155284(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Specifies the function that creates a date.'
tags:
  - JS
  - Basic
uri: javascript/Date/constructor

---
## <span>Summary</span>

Specifies the function that creates a date.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    date.constructor

## <span>Examples</span>

The following example illustrates the use of the constructor property.

``` js
var x = new Date("Hi");

 if (x.constructor == Date)
     document.write("Object is a date.");

 // Output:
 // Object is a date.
```

## <span>Remarks</span>

The required date is the name of a date object.

The **constructor** property is a member of the prototype of every object that has a prototype. The **constructor** property contains a reference to the function that constructs instances of that particular object.

