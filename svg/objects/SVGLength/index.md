---
title: SVGLength
tags:
  - API
  - Objects
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'Unreviewed MSDN import'
uri: svg/objects/SVGLength

---
# SVGLength

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

You can designate an **SVGLength** object as read-only, so that attempts to modify the object raises an **NoModificationAllowedError** exception.

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.11

### Members

The **SVGLength** object has these methods:

-   [**convertToSpecifiedUnits**](/svg/methods/convertToSpecifiedUnits): Changes the stored unit identifier to the specified type.
-   [**newValueSpecifiedUnits**](/svg/methods/newValueSpecifiedUnits): Resets the specified value as a number with the specified **unit type**, replacing the values for all of the attributes on the object.

The **SVGLength** object has these properties:

-   [**unitType**](/svg/properties/unitType_(SVGLength)): Gets or sets a value that indicates the type of length units.
-   [**value**](/svg/properties/value): Gets or sets the value of the given attribute.
-   [**valueAsString**](/svg/properties/valueAsString): Gets or sets the string form of the [**value**](/svg/properties/value) property, in the units that **svgUnitTypes** specifies.
-   [**valueInSpecifiedUnits**](/svg/properties/valueInSpecifiedUnits): Gets or sets the length or angle value, as a floating point number, in the units that **svgUnitTypes** specifies.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

