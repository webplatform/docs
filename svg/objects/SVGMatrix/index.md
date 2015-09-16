---
title: SVGMatrix
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: SVGElement
    href: /svg/objects/SVGElement
standardization_status: Unknown
tags:
  - API
  - Objects
  - DOM
uri: svg/objects/SVGMatrix

---
Inherits from [SVGElement](/svg/objects/SVGElement)[SVGElement](/svg/objects/SVGElement)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from SVGElement

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Many SVG graphics operations use **2×3** matrices. When you need a matrix for matrix arithmetic, you can expand a **2×3** matrix into a **3×3** matrix equivalent by adding a third row of **[0 0 1]**.

### Standards information

-   [Scalable Vector Graphics: Coordinate Systems, Transformations and Units](http://go.microsoft.com/fwlink/p/?linkid=204735), Section 7.14.3

### Members

The **SVGMatrix** object has these methods:

-   [**flipX**](/svg/methods/flipX): Returns a matrix equivalent to a flip about the x-axis.
-   [**flipY**](/svg/methods/flipY): Returns a matrix equivalent to a flip about the y-axis.
-   [**inverse**](/svg/methods/inverse): Returns the inverse of this matrix.
-   [**multiply**](/svg/methods/multiply): Post-multiplies the matrix by the specified second matrix and returns the resulting matrix.
-   [**rotate**](/svg/methods/rotate): Post-multiplies a rotation transformation on the current matrix and returns the resulting matrix.
-   [**rotateFromVector**](/svg/methods/rotateFromVector): Post-multiplies the matrix by a specified rotation transformation and returns the resulting matrix.
-   [**scale**](/svg/methods/scale): Post-multiplies the matrix by a uniform scale transformation and returns the resulting matrix.
-   [**scaleNonUniform**](/svg/methods/scaleNonUniform): Post-multiplies the matrix by a non-uniform scale transformation and returns the resulting matrix.
-   [**skewX**](/svg/methods/skewX): Post-multiplies the matrix by a skew transformation along the x-axis and returns the resulting matrix.
-   [**skewY**](/svg/methods/skewY): Post-multiplies the matrix by a skew transformation along the y-axis and returns the resulting matrix.
-   [**translate**](/svg/methods/translate): Post-multiplies the matrix by a translation transformation and returns the resulting matrix.

The **SVGMatrix** object has these properties:

-   [**a**](/svg/properties/a): Gets or sets the **a** entry of the **SVGMatrix**.
-   [**b**](/svg/properties/b): Gets or sets the **b** entry of the **SVGMatrix**.
-   [**c**](/svg/properties/c): Gets or sets the **c** entry of the **SVGMatrix**.
-   [**d**](/svg/properties/d): Gets or sets the **d** entry of the **SVGMatrix**.
-   [**e**](/svg/properties/e): Gets or sets the **e** entry of the **SVGMatrix**.
-   [**f**](/svg/properties/f): Gets or sets the [**f**](/svg/properties/f) entry of the **SVGMatrix**.
