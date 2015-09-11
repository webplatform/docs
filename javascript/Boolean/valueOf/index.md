---
title: valueOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155288(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the primitive value of the specified boolean.'
tags:
  - JS
  - Basic
uri: javascript/Boolean/valueOf

---
## <span>Summary</span>

Returns the primitive value of the specified boolean.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    boolean.valueOf()

## <span>Return Value</span>

The primitive value (true or false) of the Boolean.

## <span>Examples</span>

The following code shows how to use this method.

``` js
var bool = new Boolean("true");
 var s = bool.valueOf();
 document.write(s);

 // Output: true
```

