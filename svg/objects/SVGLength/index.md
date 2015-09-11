---
title: SVGLength
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
uri: svg/objects/SVGLength

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

You can designate an **SVGLength** object as read-only, so that attempts to modify the object raises an **NoModificationAllowedError** exception.

### <span>Standards information</span>

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.11

### <span>Members</span>

The **SVGLength** object has these methods:

-   [**convertToSpecifiedUnits**](/svg/methods/convertToSpecifiedUnits): Changes the stored unit identifier to the specified type.
-   [**newValueSpecifiedUnits**](/svg/methods/newValueSpecifiedUnits): Resets the specified value as a number with the specified **unit type**, replacing the values for all of the attributes on the object.

The **SVGLength** object has these properties:

-   [**unitType**](/svg/properties/unitType_(SVGLength)): Gets or sets a value that indicates the type of length units.
-   [**value**](/svg/properties/value): Gets or sets the value of the given attribute.
-   [**valueAsString**](/svg/properties/valueAsString): Gets or sets the string form of the [**value**](/svg/properties/value) property, in the units that **svgUnitTypes** specifies.
-   [**valueInSpecifiedUnits**](/svg/properties/valueInSpecifiedUnits): Gets or sets the length or angle value, as a floating point number, in the units that **svgUnitTypes** specifies.
