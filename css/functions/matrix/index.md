---
title: matrix()
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://jsfiddle.net/denbuzze/J2CLV/1/'
readiness: 'Ready to Use'
summary: 'Defines a two dimensional transformation in matrix format.'
tags:
  - CSS
  - Functions
uri: css/functions/matrix()

---
## Summary

Defines a two dimensional transformation in matrix format.

## Examples

``` css
-webkit-transform: matrix(1, 0, 0.5, 1, 10, 0);
-o-transform: matrix(1, 0, 0.5, 1, 10, 0);
transform: matrix(1, 0, 0.5, 1, 10, 0);
```

[View live example](http://jsfiddle.net/denbuzze/J2CLV/1/)

## Notes

### Remarks

This function defines a two dimensional transformation in matrix format.

That is, a function `matrix(a,b,c,d,e,f)` which holds 6 parameters as numbers, each one controlling one transformation factor. In fact, `matrix()` combines all the CSS transformation functions (translate, skew, etc.) in one command. For example, the new position of a point `(x,y)` will be such that:

    newX = a*x + c*y + e

and

    newY = b*x + d*y + f

For more information about transformation matrices, see [Mathematical Description of Transform Functions](http://go.microsoft.com/fwlink/p/?LinkId=256246), in the [CSS3 Transforms](http://go.microsoft.com/fwlink/?LinkID=223145) specification.

### Syntax

**matrix** `( <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number>  ,  <number> )`

### Parameters

*number*
:   A matrix value.

### Standards information

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.1

## See also

### Related pages (MSDN)

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
-   `Hands On: 2D Transforms`
