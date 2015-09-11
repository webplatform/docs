---
title: rotateY()
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Rotates an element around its Y-axis at a given degree.'
tags:
  - CSS
  - Functions
uri: css/functions/rotateY()

---
## <span>Summary</span>

Rotates an element around its Y-axis at a given degree.

## <span>Examples</span>

The following code snippet is an example of the **rotateY** function in use as applied to a square blue [**div**](/html/elements/div) element along with the [**perspective**](/css/functions/perspective()) function (which simulates depth).

``` css
div {
  transform: perspective(500px) rotateY(45deg);
}
```

## <span>Notes</span>

### <span>Remarks</span>

The **rotateY** transform function is the same as [**rotate3d**](/css/functions/rotate3d())(0, 1, 0, \<*angle*\>).

### <span>Syntax</span>

**rotateY** `( <angle> )`

### <span>Parameters</span>

*angle*
:   The angle by which to rotate the element about the *y*-axis. This value is expressed as a number followed by a supported angle unit.

### <span>Standards information</span>

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.2

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
-   `Hands On: 3-D Transforms`
