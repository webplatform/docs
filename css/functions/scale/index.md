---
title: scale()
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines a 2D scale transformation.'
tags:
  - CSS
  - Functions
uri: css/functions/scale()

---
## <span>Summary</span>

Defines a 2D scale transformation.

## <span>Examples</span>

The following code snippet is an example of the **scale** function in use as applied to a square blue [**div**](/html/elements/div) element.

``` css
div {
  transform: scale(1.65, 0.6);
}
```

## <span>Notes</span>

### <span>Remarks</span>

If the second parameter is not provided, it is takes a value equal to the first. The function **scale**(1, 1) leaves the element unchanged, while **scale**(2, 2) causes it to appear twice as long in both the *x*- and *y*-axes, or four times its original size.

### <span>Syntax</span>

**scale** `( <scaling-value-x>  [ ,  <scaling-value-y>  ])`

### <span>Parameters</span>

*scaling-value-x*
:   Numerical value by which to scale the specified element in the *x*-direction.
*scaling-value-y*
:   Optional. Numerical value by which to scale the specified element in the *y*-direction.

## <span>Related specifications</span>

[CSS Transforms Module Level 3](http://www.w3.org/TR/css3-transforms/)
:   Working Draft

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Hands On: 2D Transforms`
