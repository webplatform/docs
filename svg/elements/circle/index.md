---
title: circle
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The circle element is an SVG basic shape, used to create circles based on a center point and a radius.'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/circle

---
## Summary

The circle element is an SVG basic shape, used to create circles based on a center point and a radius.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, the circle element is used to draw a tomato-colored circle with radius 50.

``` html
<svg width="400" height="400">
  <circle cx="100" cy="100" r="50" fill="tomato" />
</svg>
```

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The arc of a **circle** element begins at the 3 o'clock point on the radius and progresses towards the 9 o'clock point. The starting point and direction of the arc are affected by the user space transform in the same manner as the geometry of the element.

### Standards information

-   [Scalable Vector Graphics: Basic Shapes](http://www.w3.org/TR/SVG11/shapes.html#InterfaceSVGCircleElement), Section 9.8.2

### Members

Specific attributes of **SVGCircleElement**:

-   [**cx**](/svg/properties/cx): Gets or sets the x-coordinate of the center of a circle or an ellipse.
-   [**cy**](/svg/properties/cy): Gets or sets the y-coordinate of the center of a circle or an ellipse.
-   [**r**](/svg/properties/r): Gets or sets the radius of a circle.

Global attributes of **SVGCircleElement**:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**fill**](/svg/attributes/fill): Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
-   [**fillOpacity**](/svg/attributes/fill-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
-   [**fillRule**](/svg/attributes/fill-rule): Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**pointerEvents**](/svg/attributes/pointers): Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**stroke**](/svg/attributes/stroke): Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.
-   [**strokeDasharray**](/svg/attributes/stroke-dasharray): Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.
-   [**strokeDashoffset**](/svg/attributes/stroke-dashoffset): Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.
-   [**strokeLinecap**](/svg/attributes/stroke-linecap): Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.
-   [**strokeLinejoin**](/svg/attributes/stroke-linejoin): Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.
-   [**strokeMiterlimit**](/svg/attributes/stroke-miterlimit): Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the [**strokeLinejoin**](/svg/attributes/stroke-linejoin) property).
-   [**strokeOpacity**](/svg/attributes/stroke-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.
-   [**strokeWidth**](/svg/attributes/stroke-width): Sets or retrieves a value that specifies the width of the stroke on the current object.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**transform**](/svg/properties/transform): Gets the value of a [**transform**](/svg/properties/transform) attribute.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.

The **SVGCircleElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGCircleElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

## Related specifications

[SVG 1.1](http://www.w3.org/TR/SVG/shapes.html#CircleElement)
:   W3C Recommendation

[SVG Tiny 1.2](http://www.w3.org/TR/SVGTiny12/shapes.html#CircleElement)
:   W3C Recommendation
