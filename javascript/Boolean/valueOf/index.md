---
title: 'valueOf'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155288(v=vs.94).aspx)'
compatibility:
  feature: valueOf
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns the primitive value of the specified boolean.'
tags:
  - JS
  - Basic
uri: javascript/Boolean/valueOf

---
## Summary

Returns the primitive value of the specified boolean.

## Syntax

    boolean.valueOf()

## Return Value

The primitive value (true or false) of the Boolean.

## Examples

The following code shows how to use this method.

``` js
var bool = new Boolean("true");
 var s = bool.valueOf();
 document.write(s);

 // Output: true
```

