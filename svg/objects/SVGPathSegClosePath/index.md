---
title: SVGPathSegClosePath
tags:
  - API
  - Objects
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'Unreviewed MSDN import'
uri: svg/objects/SVGPathSegClosePath

---
# SVGPathSegClosePath

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

The closepath command (**Z** or **z**) ends the current subpath and causes an automatic straight line to be drawn from the current point to the initial point of the current subpath. If you follow a "closepath" command immediately by a "moveto" command, the "moveto" command identifies the start point of the next subpath. If you follow a "closepath" command immediately by any other command, the next subpath starts at the same initial point as the current subpath.

When a subpath ends in a "closepath" command, the implementation of 'stroke-linejoin' and 'stroke-linecap' differs from when you manually close a subpath through a "lineto" command. With a "closepath" command, the end of the final segment of the subpath is joined with the start of the initial segment of the subpath by using the current value of 'stroke-linejoin'. If you manually close the subpath through a "lineto" command, the start of the first segment and the end of the last segment are each capped by using the current value of 'stroke-linecap' instead of being joined. At the end of the command, the new current point is set to the initial point of the current subpath.

### Standards information

-   [Scalable Vector Graphics: Paths](http://go.microsoft.com/fwlink/p/?linkid=204736), Section 8.5.2

### Members

The **SVGPathSegClosePath** object has these properties:

-   [**pathSegType**](/svg/properties/pathSegType): Gets the type of the path segment.
-   [**pathSegTypeAsLetter**](/svg/properties/pathSegTypeAsLetter): Gets the type of the path segment, specified by the corresponding one-character command name.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

