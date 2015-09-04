---
title: SVGPathSegCurvetoQuadraticSmoothAbs
tags:
  - API
  - Objects
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'Unreviewed MSDN import'
uri: svg/objects/SVGPathSegCurvetoQuadraticSmoothAbs

---
# SVGPathSegCurvetoQuadraticSmoothAbs

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[SVGElement](/svg/objects/SVGElement)</span></span>

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

The **T** object uses absolute coordinates to draw a quadratic Bézier curve from the current point to (x,y). The control point is the reflection of the control point on the previous command, relative to the current point. (If there is no previous command or if the previous command was not a **Q**, **q**, **T** or **t** command, assume that the control point is coincident with the current point.) At the end of the command, the new current point becomes the final (x,y) coordinate pair that is used in the polybézier.

### Standards information

-   [Scalable Vector Graphics: Paths](http://go.microsoft.com/fwlink/p/?linkid=204736), Section 8.5.19

### Members

The **SVGPathSegCurvetoQuadraticSmoothAbs** object has these properties:

-   [**pathSegType**](/svg/properties/pathSegType): Gets the type of the path segment.
-   [**pathSegTypeAsLetter**](/svg/properties/pathSegTypeAsLetter): Gets the type of the path segment, specified by the corresponding one-character command name.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

