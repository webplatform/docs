---
title: 'SVGAngle'
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
tags:
  - API_Objects
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: svg/objects/SVGAngle

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

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.15

### Members

The **SVGAngle** object has these methods:

-   [**convertToSpecifiedUnits**](/svg/methods/convertToSpecifiedUnits): Changes the stored unit identifier to the specified type.
-   [**newValueSpecifiedUnits**](/svg/methods/newValueSpecifiedUnits): Resets the specified value as a number with the specified **unit type**, replacing the values for all of the attributes on the object.

The **SVGAngle** object has these properties:

-   [**unitType**](/svg/properties/unitType): Gets or sets a value that indicates the type of angle units.
-   [**value**](/svg/properties/value): Gets or sets the value of the given attribute.
-   [**valueAsString**](/svg/properties/valueAsString): Gets or sets the string form of the [**value**](/svg/properties/value) property, in the units that **svgUnitTypes** specifies.
-   [**valueInSpecifiedUnits**](/svg/properties/valueInSpecifiedUnits): Gets or sets the length or angle value, as a floating point number, in the units that **svgUnitTypes** specifies.
