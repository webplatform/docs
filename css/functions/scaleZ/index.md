---
title: scaleZ()
tags:
  - CSS
  - Functions
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines a 3D scale transformation by giving a value for the Z-axis.'
uri: css/functions/scaleZ()

---
# scaleZ()

## Summary

Defines a 3D scale transformation by giving a value for the Z-axis.

## Examples

The following code snippet is an example of the **scaleZ** function in use as applied to a square blue [**div**](/html/elements/div) element along with the [**perspective**](/css/functions/perspective()) function (which simulates depth) and the [**rotateX**](/css/functions/rotateX()) function.

``` {.css}
div {
  transform: perspective(500px) scaleZ(2) rotateX(45deg);
}
```

## Notes

### Remarks

The effect of the **scaleZ** function is most evident when used in combination with functions such as the [**perspective**](/css/functions/perspective()) and [**rotate**](/css/functions/rotate()) (and related) functions.

### Syntax

**scaleZ** `( <scaling-value-z> )`

### Parameters

*scaling-value-z*
:   Numerical value by which to scale the specified element in the *z*-direction.

## Related specifications

Specification
:   Status
[CSS Transforms Module Level 3](http://www.w3.org/TR/css3-transforms/)
:   Working Draft

## See also

### Related pages (MSDN)

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
-   `Hands On: 3-D Transforms`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

