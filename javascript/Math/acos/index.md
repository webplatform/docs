---
title: 'acos'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/w1ah75x5(v=vs.94).aspx)'
compatibility:
  feature: acos
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns the arc cosine (or inverse cosine) of a number.'
tags:
  - JS_Basic
uri: javascript/Math/acos

---
## Summary

Returns the arc cosine (or inverse cosine) of a number.

## Syntax

    Math.acos( number )

**number**
:   Required. The required number argument is a numeric expression.

## Return Value

The arc cosine of the number argument, in radians.

## Examples

The following code shows how to use the **acos** function.

``` js
var v1 = Math.acos(-1.0);
 var v2 = Math.cos(-1.0);

 document.write(v1);
 document.write("<br/>");
 document.write(v2);

 // Output:
 // 3.141592653589793
 // 0.5403023058681398
```

## Remarks

**Applies To** : [Math Object](/javascript/Math)

## See also

### Other articles

-   [Math.asin Function](/javascript/Math/asin)
-   [Math.atan Function](/javascript/Math/atan)
-   [Math.cos Function](/javascript/Math/cos)
-   [Math.sin Function](/javascript/Math/sin)
-   [Math.tan Function](/javascript/Math/tan)
-   [Math Object](/javascript/Math)

