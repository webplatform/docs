---
title: SVGPoint
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
uri: svg/objects/SVGPoint

---
Inherits from [SVGElement](/svg/objects/SVGElement)[SVGElement](/svg/objects/SVGElement)

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Inherited from SVGElement</span>

### <span>Properties</span>

*No properties.*

### <span>Methods</span>

*No methods.*

### <span>Events</span>

*No events.*

## <span>Notes</span>

### <span>Remarks</span>

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

An **SVGPoint** object is an (x, y) coordinate pair. When you use an **SVGPoint** object in matrix operations, the object is treated as a vector of the following form.

### <span>Standards information</span>

-   [Scalable Vector Graphics: Coordinate Systems, Transformations and Units](http://go.microsoft.com/fwlink/p/?linkid=204735), Section 7.14.1

### <span>Members</span>

The **SVGPoint** object has these methods:

-   [**matrixTransform**](/svg/methods/matrixTransform): Applies the given 2×3 matrix transformation on this **SVGPoint** object and returns a new,

transformed **SVGPoint** object.

The **SVGPoint** object has these properties:

-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.
