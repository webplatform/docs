---
title: 'path'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: path
  topic: svg
notes:
  - 'Needs spec reference, standardization status, fix table code in Notes'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
summary: 'The path element is the generic element to define a shape.'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/path

---
## Summary

The path element is the generic element to define a shape.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, the path element is used to create a red curved path.

``` html


<svg width="400" height="400">
  <path d="M 50,100 Q 150,50 250,100" stroke="red" stroke-width="10" fill="white"/>
</svg>
```

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Path data can contain newline characters and thus can be broken up into multiple lines to improve readability. Because of line-length limitations with certain related tools, it is recommended to split long path data strings across multiple lines, with each line not exceeding 255 characters. Also note that newline characters are allowed only at certain places within path data.

The syntax of path data is concise in order to allow for minimal file size and efficient downloads, because many SVG files will be dominated by their path data. Some of the ways that SVG attempts to minimize the size of path data are as follows:

-   All instructions are expressed as one character (for example, a *moveto* is expressed as an **M**).

-   Superfluous white space and separators such as commas can be eliminated (for example, "M 100 100 L 200 200" contains unnecessary spaces and could be expressed more compactly as "M100 100L200 200").

-   The command letter can be eliminated on subsequent commands if the same command is used multiple times in a row (for example, you can drop the second **L** in "M 100 200 L 200 100 **L** -100 -200" and use "M 100 200 L 200 100 -100 -200" instead).

-   Relative versions of all commands are available (uppercase means absolute coordinates, lowercase means relative coordinates).
-   Alternate forms of *lineto* are available to optimize the special cases of horizontal and vertical lines (absolute and relative).

-   Alternate forms of *curve* are available to optimize the special cases where some of the control points on the current segment can be determined automatically from the control points on the previous segment.

The path-data syntax is a prefix notation (that is, commands followed by parameters). The only allowable decimal point is a Unicode U+0046 FULL STOP (".") character (also referred to in Unicode as PERIOD, dot, and decimal point) and no other delimiter characters are allowed. (For example, the following is an invalid numeric value in a path data stream: "13,000.56". Instead, say: "13000.56".)

For the relative versions of the commands, all coordinate values are relative to the current point at the start of the command. For example, the absolute version of *moveto* is **M** whereas its relative form is indicated with a lowercase **m**. Absolute versus relative path commands are discussed in the following table.

**Note:** In the Path Command Table below, the following notation is used.

{

### Standards information

-   [Scalable Vector Graphics: Paths](http://www.w3.org/TR/SVG11/paths.html), Section 8.5.23

### Members

The **SVGPathElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGPathElement** object has these methods:

-   [**createSVGPathSegArcAbs**](/svg/methods/createSVGPathSegArcAbs): Returns a stand-alone, parentless [**SVGPathSegArcAbs**](/svg/objects/SVGPathSegArcAbs) object.
-   [**createSVGPathSegArcRel**](/svg/methods/createSVGPathSegArcRel): Returns a stand-alone, parentless [**SVGPathSegArcRel**](/svg/objects/SVGPathSegArcRel) object.
-   [**createSVGPathSegClosePath**](/svg/methods/createSVGPathSegClosePath): Returns a stand-alone, parentless [**SVGPathSegClosePath**](/svg/objects/SVGPathSegClosePath) object.
-   [**createSVGPathSegCurvetoCubicAbs**](/svg/methods/createSVGPathSegCurvetoCubicAbs): Returns a stand-alone, parentless [**SVGPathSegCurvetoCubicAbs**](/svg/objects/SVGPathSegCurvetoCubicAbs) object.
-   [**createSVGPathSegCurvetoCubicRel**](/svg/methods/createSVGPathSegCurvetoCubicRel): Returns a stand-alone, parentless [**SVGPathSegCurvetoCubicRel**](/svg/objects/SVGPathSegCurvetoCubicRel) object.
-   [**createSVGPathSegCurvetoCubicSmoothAbs**](/svg/methods/createSVGPathSegCurvetoCubicSmoothAbs): Returns a stand-alone, parentless [**SVGPathSegCurvetoCubicSmoothAbs**](/svg/objects/SVGPathSegCurvetoCubicSmoothAbs) object.
-   [**createSVGPathSegCurvetoCubicSmoothRel**](/svg/methods/createSVGPathSegCurvetoCubicSmoothRel): Returns a stand-alone, parentless [**SVGPathSegCurvetoCubicSmoothRel**](/svg/objects/SVGPathSegCurvetoCubicSmoothRel) object.
-   [**createSVGPathSegCurvetoQuadraticAbs**](/svg/methods/createSVGPathSegCurvetoQuadraticAbs): Returns a stand-alone, parentless [**SVGPathSegCurvetoQuadraticAbs**](/svg/objects/SVGPathSegCurvetoQuadraticAbs) object.
-   [**createSVGPathSegCurvetoQuadraticRel**](/svg/methods/createSVGPathSegCurvetoQuadraticRel): Returns a stand-alone, parentless [**SVGPathSegCurvetoQuadraticRel**](/svg/objects/SVGPathSegCurvetoQuadraticRel) object.
-   [**createSVGPathSegCurvetoQuadraticSmoothAbs**](/svg/methods/createSVGPathSegCurvetoQuadraticSmoothAbs): Returns a stand-alone, parentless [**SVGPathSegCurvetoQuadraticSmoothAbs**](/svg/objects/SVGPathSegCurvetoQuadraticSmoothAbs) object.
-   [**createSVGPathSegCurvetoQuadraticSmoothRel**](/svg/methods/createSVGPathSegCurvetoQuadraticSmoothRel): Returns a stand-alone, parentless [**SVGPathSegCurvetoQuadraticSmoothRel**](/svg/objects/SVGPathSegCurvetoQuadraticSmoothRel) object.
-   [**createSVGPathSegLinetoAbs**](/svg/methods/createSVGPathSegLinetoAbs): Returns a stand-alone, parentless [**SVGPathSegLinetoAbs**](/svg/objects/SVGPathSegLinetoAbs) object.
-   [**createSVGPathSegLinetoHorizontalAbs**](/svg/methods/createSVGPathSegLinetoHorizontalAbs): Returns a stand-alone, parentless [**SVGPathSegLinetoHorizontalAbs**](/svg/objects/SVGPathSegLinetoHorizontalAbs) object.
-   [**createSVGPathSegLinetoHorizontalRel**](/svg/methods/createSVGPathSegLinetoHorizontalRel): Returns a stand-alone, parentless [**SVGPathSegLinetoHorizontalRel**](/svg/objects/SVGPathSegLinetoHorizontalRel) object.
-   [**createSVGPathSegLinetoRel**](/svg/methods/createSVGPathSegLinetoRel): Returns a stand-alone, parentless [**SVGPathSegLinetoRel**](/svg/objects/SVGPathSegLinetoRel) object.
-   [**createSVGPathSegLinetoVerticalAbs**](/svg/methods/createSVGPathSegLinetoVerticalAbs): Returns a stand-alone, parentless [**SVGPathSegLinetoVerticalAbs**](/svg/objects/SVGPathSegLinetoVerticalAbs) object.
-   [**createSVGPathSegLinetoVerticalRel**](/svg/methods/createSVGPathSegLinetoVerticalRel): Returns a stand-alone, parentless [**SVGPathSegLinetoVerticalRel**](/svg/objects/SVGPathSegLinetoVerticalRel) object.
-   [**createSVGPathSegMovetoAbs**](/svg/methods/createSVGPathSegMovetoAbs): Returns a standalone parentless [**SVGPathSegMovetoAbs**](/svg/objects/SVGPathSegMovetoAbs) object.
-   [**createSVGPathSegMovetoRel**](/svg/methods/createSVGPathSegMovetoRel): Returns a stand-alone, parentless [**SVGPathSegMovetoRel**](/svg/objects/SVGPathSegMovetoRel) object.
-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getPathSegAtLength**](/svg/methods/getPathSegAtLength): Gets the index of [**pathSegList**](/svg/properties/pathSegList) by using the specified distance along the path.
-   [**getPointAtLength**](/svg/methods/getPointAtLength): Gets the (x,y) coordinate in user space that is the specified distance along the path.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTotalLength**](/svg/methods/getTotalLength): Gets the total length of the path, as a distance in the current user coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGPathElement** object has these properties:

-   [**animatedNormalizedPathSegList**](/svg/properties/animatedNormalizedPathSegList): Gets or sets the normalized animated contents of

the [**d**](/svg/properties/d) attribute.

-   [**animatedPathSegList**](/svg/properties/animatedPathSegList): Gets or sets the animated contents of the [**d**](/svg/properties/d) attribute in a form that matches the SVG syntax.
-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**fill**](/svg/attributes/fill): Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
-   [**fillOpacity**](/svg/attributes/fill-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
-   [**fillRule**](/svg/attributes/fill-rule): Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**marker**](/svg/attributes/marker): Sets or retrieves a value that specifies the marker symbol that is used for all vertices on the given **path** element or basic shape.
-   [**markerEnd**](/svg/attributes/marker-end): Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the final vertex of a given **path** element or basic shape.
-   [**markerMid**](/svg/attributes/marker-mid): Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at every other vertex (that is, every vertex except the first and last) of a given **path** element or basic shape.
-   [**markerStart**](/svg/attributes/marker-start): Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the first vertex of a given **path** element or basic shape.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**normalizedPathSegList**](/svg/properties/normalizedPathSegList): Gets or sets the normalized static contents of the [**d**](/svg/properties/d) attribute.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.

## Related specifications

[SVG 1.1](http://www.w3.org/TR/SVG11/paths.html)
:   W3C Recommendation
