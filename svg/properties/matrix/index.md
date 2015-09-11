---
title: matrix
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/matrix

---
## <span>Notes</span>

### <span>Remarks</span>

The matrix object is *live* (that is, any changes to the [**SVGTransform**](/svg/objects/SVGTransform) object are immediately reflected in the matrix object and vice versa). If you change the matrix object directly (that is, without using the **SVGTransform** methods), the **SVGTransform** type changes to SVG\_TRANSFORM\_MATRIX.

The values in the returned matrix changes based on the type of matrix:

-   For a SVG\_TRANSFORM\_MATRIX matrix, the matrix contains the [**a**](/svg/properties/a), [**b**](/svg/properties/b), [**c**](/svg/properties/c), [**d**](/svg/properties/d), [**e**](/svg/properties/e), and [**f**](/svg/properties/f) values that the user supplies.

-   For a SVG\_TRANSFORM\_TRANSLATE matrix, the [**e**](/svg/properties/e) and [**f**](/svg/properties/f) values represent the translation amounts ([**a**](/svg/properties/a)=1, [**b**](/svg/properties/b)=0, [**c**](/svg/properties/c)=0, and [**d**](/svg/properties/d)=1).

-   For a SVG\_TRANSFORM\_SCALE matrix, the [**a**](/svg/properties/a) and [**d**](/svg/properties/d) values represent the translation amounts ([**b**](/svg/properties/b)=0, [**c**](/svg/properties/c)=0, [**e**](/svg/properties/e)=0, and [**f**](/svg/properties/f)=0).

-   For a SVG\_TRANSFORM\_ROTATE, SVG\_TRANSFORM\_SKEWX, or SVG\_TRANSFORM\_SKEWY matrix, the [**a**](/svg/properties/a), [**b**](/svg/properties/b), [**c**](/svg/properties/c), and [**d**](/svg/properties/d) values represent the matrix that causes the given transformation ([**e**](/svg/properties/e)=0 and [**f**](/svg/properties/f)=0).

### <span>Syntax</span>

### <span>Standards information</span>

-   [Scalable Vector Graphics: Coordinate Systems, Transformations and Units](http://go.microsoft.com/fwlink/p/?linkid=204735), Section 7.14.4

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGTransform**](/svg/objects/SVGTransform)
