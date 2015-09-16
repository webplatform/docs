---
title: 'SVGPathSegArcAbs'
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
uri: svg/objects/SVGPathSegArcAbs

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

The **A** command uses absolute coordinates to draw an elliptical arc from the current point to (x, y). The size and orientation of the ellipse are defined by two radius values ([**rx**](/svg/properties/rx_(SVGEllipseElement)), [**ry**](/svg/properties/ry_(SVGEllipseElement))) and a rotationa bout the x-axis, which indicates how the ellipse is rotated relative to the current coordinate system. The center ([**cx**](/svg/properties/cx), [**cy**](/svg/properties/cy)) of the ellipse is calculated automatically to meet the constraints from the other parameters. large-arc-flag and sweep-flag contribute to the automatic calculations and help determine how the arc is drawn.

### Standards information

-   [Scalable Vector Graphics: Paths](http://go.microsoft.com/fwlink/p/?linkid=204736), Section 8.5.11

### Members

The **SVGPathSegArcAbs** object has these properties:

-   [**angle**](/svg/properties/angle): Gets or sets a value that indicates an angle unit.
-   [**largeArcFlag**](/svg/properties/largeArcFlag): Gets or sets the value of the large-arc-flag parameter.
-   [**pathSegType**](/svg/properties/pathSegType): Gets the type of the path segment.
-   [**pathSegTypeAsLetter**](/svg/properties/pathSegTypeAsLetter): Gets the type of the path segment, specified by the corresponding one-character command name.
-   [**r1**](/svg/properties/r1): Gets or sets the x-axis radius for an ellipse that is associated with a [**path**](/svg/elements/path) element.
-   [**r2**](/svg/properties/r2): Gets or sets the y-axis radius for an ellipse that is associated with a [**path**](/svg/elements/path) element.
-   [**sweepFlag**](/svg/properties/sweepFlag): Gets or sets the value of the sweep-flag parameter.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.
