---
title: atan2
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/a5h904dw(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the angle (in radians) from the X axis to a point ( y , x ).'
tags:
  - JS
  - Basic
uri: javascript/Math/atan2

---
## <span>Summary</span>

Returns the angle (in radians) from the X axis to a point ( y , x ).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    Math.atan2( y , x )

**x**
:   Required. A numeric expression representing the cartesian x-coordinate.

**y**
:   Required. A numeric expression representing the cartesian y-coordinate.

## <span>Examples</span>

``` js
var v1 = Math.atan2(2,3);
document.write(v1);
// Output: 0.5880026035475675
```

## <span>Remarks</span>

The return value is between -pi and pi. It represents the angle of the supplied ( y , x ) point, in radians.

**Applies To** : [Math Object](/javascript/Math)

## <span>See also</span>

### <span>Other articles</span>

-   [Math.atan Function](/javascript/Math/atan)
-   [Math.tan Function](/javascript/Math/tan)
-   [Math Object](/javascript/Math)

