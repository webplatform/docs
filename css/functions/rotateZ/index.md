---
title: rotateZ()
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Rotates an element around its Z-axis at a given degree.'
tags:
  - CSS
  - Functions
uri: css/functions/rotateZ()

---
## Summary

Rotates an element around its Z-axis at a given degree.

## Examples

The following code snippet is an example of the **rotateZ** function in use as applied to a square blue [**div**](/html/elements/div) element.

``` css
div {
  transform: rotateZ(45deg);
}
```

## Notes

### Remarks

The **rotateZ** transform function is the same as [**rotate3d**](/css/functions/rotate3d())(0, 0, 1, \<*angle*\>).

### Syntax

**rotateZ** `( <angle> )`

### Parameters

*angle*
:   The angle by which to rotate the element about the *z*-axis. This value is expressed as a number followed by a supported angle unit.

### Standards information

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.2

## See also

### Related pages

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
-   `Hands On: 3-D Transforms`
