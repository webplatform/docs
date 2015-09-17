---
title: 'scale()'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: scale()
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines a 2D scale transformation.'
tags:
  - CSS_Functions
  - CSS
uri: css/functions/scale()

---
## Summary

Defines a 2D scale transformation.

## Examples

The following code snippet is an example of the **scale** function in use as applied to a square blue [**div**](/html/elements/div) element.

``` css
div {
  transform: scale(1.65, 0.6);
}
```

## Notes

### Remarks

If the second parameter is not provided, it is takes a value equal to the first. The function **scale**(1, 1) leaves the element unchanged, while **scale**(2, 2) causes it to appear twice as long in both the *x*- and *y*-axes, or four times its original size.

### Syntax

**scale** `( <scaling-value-x>  [ ,  <scaling-value-y>  ])`

### Parameters

*scaling-value-x*
:   Numerical value by which to scale the specified element in the *x*-direction.
*scaling-value-y*
:   Optional. Numerical value by which to scale the specified element in the *y*-direction.

## Related specifications

[CSS Transforms Module Level 3](http://www.w3.org/TR/css3-transforms/)
:   Working Draft

## See also

### Related pages

-   `Transform Functions`
-   Mathematical Description of Transform Functions[Mathematical Description of Transform Functions](http://go.microsoft.com/fwlink/p/?LinkId=256246)
-   Hands On: 2D Transforms[Hands On: 2D Transforms](http://go.microsoft.com/fwlink/?LinkID=240163)
