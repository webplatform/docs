---
title: min
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
readiness: 'Ready to Use'
summary: 'Returns the smaller of a set of numeric expressions.'
tags:
  - JS
  - Basic
uri: javascript/Math/min

---
## <span>Summary</span>

Returns the smaller of a set of numeric expressions.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    Math.min([ number1 [, number2 [... [, numberN ]]]])

## <span>Examples</span>

The following code shows how to get the smaller of two expressions.

``` js
var x = Math.min(107 - 3, 48 * 90);
 document.write(x);

 // Output:
 // 104
```

## <span>Remarks</span>

The optional number1, number2, ..., numberN arguments are numeric expressions to be evaluated.

If no arguments are provided, the return value is equal to [Number.POSITIVE\_INFINITY](/javascript/Number/constants). If any argument is **NaN** , the return value is also **NaN**.

## <span>See also</span>

### <span>Other articles</span>

-   [Math.max Function](/javascript/Math/max)

