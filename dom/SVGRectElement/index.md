---
title: 'SVGRectElement'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[SVGRectElement](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/rect) Article]'
  - 'Microsoft Developer Network: [[SVGRectElement](http://msdn.microsoft.com/en-us/library/ie/ff972117(v=vs.85).aspx) Article]'
notes:
  - 'Needs some inline SVG examples...'
readiness: 'Almost Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: SVGElement
    href: /dom/SVGElement
standardization_status: 'W3C Recommendation'
summary: 'The SVGRectElement interface provides access to the properties of the rect element.'
tags:
  - API
  - Objects
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - svg/properties/rx
    - svg/properties/ry
uri: dom/SVGRectElement

---
## Summary

The SVGRectElement interface provides access to the properties of the rect element.

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

    <rect x="10" y="10" width="100" height="100"/>

</svg>
```

``` html
<?xml version="1.0"?>
<svg width="120" height="120"
     viewPort="0 0 120 120" version="1.1"
     xmlns="http://www.w3.org/2000/svg">

    <rect x="10" y="10"
          width="100" height="100"
          rx="15" ry="15"/>

</svg>
```

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.1

### Members

The **SVGRectElement** object has these properties:

-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.
-   [**rx**](/w/index.php?title=svg/properties/rx&action=edit&redlink=1): Gets or sets the x-axis radius of a rounded corner rectangle.
-   [**ry**](/w/index.php?title=svg/properties/ry&action=edit&redlink=1): Gets or sets the y-axis radius of a rounded corner rectangle.
