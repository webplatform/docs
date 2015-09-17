---
title: 'SVGLineElement'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[SVGLineElement](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/line) Article]'
  - 'Microsoft Developer Network: [[SVGLineElement](http://msdn.microsoft.com/en-us/library/ie/ff972079(v=vs.85).aspx) Article]'
notes:
  - 'needs example'
readiness: 'Almost Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: SVGElement
    href: /dom/SVGElement
standardization_status: 'W3C Recommendation'
summary: 'Defines a line by using beginning and ending (x,y) coordinate values with stroke and stroke-width styles .'
tags:
  - API_Objects
  - DOM
uri: dom/SVGLineElement

---
## Summary

Defines a line by using beginning and ending (x,y) coordinate values with stroke and stroke-width styles .

Inherits from [SVGElement](/dom/SVGElement)[SVGElement](/dom/SVGElement)

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

## Inherited from SVGTests

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Inherited from SVGLangSpace

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Inherited from SVGExternalResourcesRequired

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Inherited from SVGStylable

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Inherited from SVGTransformable

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Examples

``` html
<?xml version="1.0"?>
<svg width="120" height="120"
     viewPort="0 0 120 120" version="1.1"
     xmlns="http://www.w3.org/2000/svg">

    <line x1="20" y1="100"
          x2="100" y2="20"
          stroke="black"
          stroke-width="2"/>

</svg>
```

``` html
<?xml version="1.0"?>
<svg xmlns="http://www.w3.org/2000/svg">
    <line x1="20" y1="100" x2="100" y2="100" stroke-width="2"
    stroke="black" transform="rotate(-45 20 100)"/>
</svg>
```

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.1

### Members

The **SVGElement** object has these properties:

-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**id**](/svg/properties/id): Standard XML attribute for assigning a unique name to an element.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor **svg** element.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
