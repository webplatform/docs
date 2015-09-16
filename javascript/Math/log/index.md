---
title: log
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
readiness: 'Ready to Use'
summary: 'Returns the natural logarithm (base e ) of a number.'
tags:
  - JS
  - Basic
uri: javascript/Math/log

---
## Summary

Returns the natural logarithm (base e ) of a number.

## Syntax

<span class="language">JavaScript</span>

    Math.log( number )

**number**
:   A number.

## Return Value

If number is positive, this function returns the natural logarithm of the number. If number is negative, this function returns NaN. If number is 0, this function returns -Infinity.

## Examples

The following code shows how to use this function.

``` js
var numArr = [ 45.3, 69.0, 557.04, 0.222 ];

 for (i in numArr) {
     document.write(Math.log(numArr[i]));
     document.write("<br/>");
 }

 // Output:
 // 3.8133070324889884
 // 4.23410650459726
 // 6.322637050634291
 // -1.5050778971098575
```

## See also

### Other articles

-   [Math.sqrt Function](/javascript/Math/sqrt)

