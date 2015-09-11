---
title: SVGTransform
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
uri: svg/objects/SVGTransform

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

### <span>Standards information</span>

-   [Scalable Vector Graphics: Coordinate Systems, Transformations and Units](http://go.microsoft.com/fwlink/p/?linkid=204735), Section 7.14.4

### <span>Members</span>

The **SVGTransform** object has these methods:

-   [**setMatrix**](/svg/methods/setMatrix): Sets the transform type to SVG\_TRANSFORM\_MATRIX by using the specified new transformation.
-   [**setRotate**](/svg/methods/setRotate): Sets the transform type to SVG\_TRANSFORM\_ROTATE by using the specified rotation angle and center of rotation.
-   [**setScale**](/svg/methods/setScale): Sets the transform type to SVG\_TRANSFORM\_SCALE by using the specified scale amounts.
-   [**setSkewX**](/svg/methods/setSkewX): Sets the transform type to SVG\_TRANSFORM\_SKEWX, with the given angle defining the amount of skew.
-   [**setSkewY**](/svg/methods/setSkewY): Sets the transform type to SVG\_TRANSFORM\_SKEWY, with the given angle defining the amount of skew.
-   [**setTranslate**](/svg/methods/setTranslate): Sets the transform type to SVG\_TRANSFORM\_TRANSLATE by using the specified components.

The **SVGTransform** object has these properties:

-   [**angle**](/svg/properties/angle): Gets or sets a value that indicates an angle unit.
-   [**matrix**](/svg/properties/matrix): Gets the matrix that represents this transformation.
-   [**type**](/svg/properties/type_(SVGTransform)): Gets or sets the **transform** attribute type.
