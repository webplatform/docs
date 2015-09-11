---
title: scaleZ()
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines a 3D scale transformation by giving a value for the Z-axis.'
tags:
  - CSS
  - Functions
uri: css/functions/scaleZ()

---
## <span>Summary</span>

Defines a 3D scale transformation by giving a value for the Z-axis.

## <span>Examples</span>

The following code snippet is an example of the **scaleZ** function in use as applied to a square blue [**div**](/html/elements/div) element along with the [**perspective**](/css/functions/perspective()) function (which simulates depth) and the [**rotateX**](/css/functions/rotateX()) function.

``` css
div {
  transform: perspective(500px) scaleZ(2) rotateX(45deg);
}
```

## <span>Notes</span>

### <span>Remarks</span>

The effect of the **scaleZ** function is most evident when used in combination with functions such as the [**perspective**](/css/functions/perspective()) and [**rotate**](/css/functions/rotate()) (and related) functions.

### <span>Syntax</span>

**scaleZ** `( <scaling-value-z> )`

### <span>Parameters</span>

*scaling-value-z*
:   Numerical value by which to scale the specified element in the *z*-direction.

## <span>Related specifications</span>

[CSS Transforms Module Level 3](http://www.w3.org/TR/css3-transforms/)
:   Working Draft

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
-   `Hands On: 3-D Transforms`
