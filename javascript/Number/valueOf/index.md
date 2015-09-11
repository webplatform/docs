---
title: valueOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj159595(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the primitive value of the specified number.'
tags:
  - JS
  - Basic
uri: javascript/Number/valueOf

---
## <span>Summary</span>

Returns the primitive value of the specified number.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    number.valueOf()

## <span>Return Value</span>

Returns the number.

## <span>Examples</span>

In the following example, the instantiated number object is the same as the return value of this method.

``` js
var num = 1234;
 var s = num.valueOf();

 if (num === s)
 document.write("same");
 else
 document.write("different");

 // Output:
 // same
```

