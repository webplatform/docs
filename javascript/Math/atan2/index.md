---
title: 'atan2'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/a5h904dw(v=vs.94).aspx)'
compatibility:
  feature: atan2
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns the angle (in radians) from the X axis to a point ( y , x ).'
tags:
  - JS_Basic
uri: javascript/Math/atan2

---
## Summary

Returns the angle (in radians) from the X axis to a point ( y , x ).

## Syntax

    Math.atan2( y , x )

**x**
:   Required. A numeric expression representing the cartesian x-coordinate.

**y**
:   Required. A numeric expression representing the cartesian y-coordinate.

## Examples

``` js
var v1 = Math.atan2(2,3);
document.write(v1);
// Output: 0.5880026035475675
```

## Remarks

The return value is between -pi and pi. It represents the angle of the supplied ( y , x ) point, in radians.

**Applies To** : [Math Object](/javascript/Math)

## See also

### Other articles

-   [Math.atan Function](/javascript/Math/atan)
-   [Math.tan Function](/javascript/Math/tan)
-   [Math Object](/javascript/Math)

