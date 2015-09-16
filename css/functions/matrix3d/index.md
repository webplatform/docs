---
title: matrix3d
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines a three-dimensional transformation in matrix format.  The function requires exactly 16 comma-separated numbers as parameters; these represent the matrix values in &quot;column-major&quot; (top to bottom, then left to right) order.'
tags:
  - CSS
  - Functions
uri: css/functions/matrix3d

---
## Summary

Defines a three-dimensional transformation in matrix format. The function requires exactly 16 comma-separated numbers as parameters; these represent the matrix values in &quot;column-major&quot; (top to bottom, then left to right) order.

## Examples

The following code snippet is an example of the **matrix3d** function in use. When applied to a square blue [**div**](/html/elements/div) element, it has the effect illustrated in the image.

``` css
div {
  transform: matrix3d(0.359127, -0.469472, 0.806613, 0, 0.190951, 0.882948, 0.428884, 0, -0.913545, 0, 0.406737, 0, 0, 0, 0, 1);
}
```

## Notes

### Remarks

All other transformation functions are based on the **matrix3d** function. It is a good idea to become familiar with transform coordinate systems and rendering before attempting to specify 3-D transforms manually.

### Syntax

**matrix3d** `( <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number> )`

### Parameters

*number*
:   A matrix value.

### Standards information

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.2

## See also

### Related pages

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
