---
title: 'SVGPathSegCurvetoCubicSmoothRel'
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
  - API_Objects
  - DOM
uri: svg/objects/SVGPathSegCurvetoCubicSmoothRel

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

The **s** object uses relative coordinates to draw a cubic Bézier curve from the current point to (x,y). The first control point is the reflection of the second control point on the previous command, relative to the current point. (If there is no previous command or if the previous command was not an **C**, **c**, **S**, or **s** command, assume that the first control point is coincident with the current point.) (x2,y2) is the second control point (that is, the control point at the end of the curve). You can specify multiple sets of coordinates to draw a polybézier. At the end of the command, the new current point becomes the final (x,y) coordinate pair that is used in the polybézier.

### Standards information

-   [Scalable Vector Graphics: Paths](http://go.microsoft.com/fwlink/p/?linkid=204736), Section 8.5.18

### Members

The **SVGPathSegCurvetoCubicSmoothRel** object has these properties:

-   [**pathSegType**](/svg/properties/pathSegType): Gets the type of the path segment.
-   [**pathSegTypeAsLetter**](/svg/properties/pathSegTypeAsLetter): Gets the type of the path segment, specified by the corresponding one-character command name.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**x2**](/svg/properties/x2): Gets or sets the absolute or relative x-coordinate for the second control point.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.
-   [**y2**](/svg/properties/y2): Gets or sets the absolute or relative y-coordinate for the second control point.
