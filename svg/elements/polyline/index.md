---
title: 'polyline'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/37caee51f773695efdd4'
compatibility:
  feature: polyline
  topic: svg
notes:
  - 'Fix multiple broken links'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGPolylineElement](/w/index.php?title=dom/SVGPolylineElement&action=edit&redlink=1)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The polyline element is a SVG basic shape to create a series of lines connecting several points. Usually, a polyline is used to create open shapes.'
tags:
  - Markup_Elements
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/SVGPolylineElement
    - svg/attributes/style
    - svg/attributes/class
    - svg/attributes/externalResourcesRequired
    - svg/attributes/transform
    - svg/attributes/points
uri: svg/elements/polyline

---
## Summary

The polyline element is a SVG basic shape to create a series of lines connecting several points. Usually, a polyline is used to create open shapes.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGPolylineElement](/w/index.php?title=dom/SVGPolylineElement&action=edit&redlink=1)

## Examples

In the following code example, the polyline element is used to draw a gold polyline inside an inline SVG element.

``` html


<svg width="400" height="400"  version="1.1" xmlns="http://www.w3.org/2000/svg">
  <polyline points="50,50 150,120 100,220 200,150" stroke="gold" stroke-width="1" fill="none" />
</svg>
```

</pre>
[View live example](http://gist.github.com/37caee51f773695efdd4)

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Typically, **polyline** elements define open shapes. **Note:** You cannot provide an odd number of coordinates.

### Attributes

#### Global attributes

-   [**Conditional processing attributes**](/svg/attributes#Conditional_Processing_Attributes)
-   [**Core attributes**](/svg/attributes#Core_Attributes)
-   [**Graphical events attributes**](/svg/attributes#Graphical_Event_Attributes)
-   [**Presentation attributes**](/svg/attributes#Presentation_Attributes)

-   [**style**](/w/index.php?title=svg/attributes/style&action=edit&redlink=1)
-   [**class**](/w/index.php?title=svg/attributes/class&action=edit&redlink=1)
-   [**externalResourcesRequired**](/w/index.php?title=svg/attributes/externalResourcesRequired&action=edit&redlink=1)
-   [**transform**](/w/index.php?title=svg/attributes/transform&action=edit&redlink=1)

#### Specific attributes

-   [**points**](/w/index.php?title=svg/attributes/points&action=edit&redlink=1)

### DOM Interface

This element implements the [**SVGPolylineElement**](/w/index.php?title=dom/SVGPolylineElement&action=edit&redlink=1) interface.

### Members

The **SVGPolylineElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGPolylineElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGPolylineElement** object has these properties:

-   [**animatedPoints**](/svg/properties/animatedPoints): Gets or sets the animated contents of the [**points**](/svg/properties/points) attribute.
-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**fill**](/svg/attributes/fill): Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
-   [**fillOpacity**](/svg/attributes/fill-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
-   [**fillRule**](/svg/attributes/fill-rule): Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**marker**](/svg/attributes/marker): Sets or retrieves a value that specifies the marker symbol that is used for all vertices on the given [**path**](/svg/elements/path) element or basic shape.
-   [**markerEnd**](/svg/attributes/marker-end): Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the final vertex of a given [**path**](/svg/elements/path) element or basic shape.
-   [**markerMid**](/svg/attributes/marker-mid): Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at every other vertex (that is, every vertex except the first and last) of a given [**path**](/svg/elements/path) element or basic shape.
-   [**markerStart**](/svg/attributes/marker-start): Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the first vertex of a given [**path**](/svg/elements/path) element or basic shape.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**pointerEvents**](/svg/attributes/pointers): Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
-   [**points**](/svg/properties/points): Gets or sets the static contents of the [**points**](/svg/properties/points) attribute.
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

## Related specifications

[The 'polyline' element](http://www.w3.org/TR/SVG11/shapes.html#PolylineElement)
:   W3C Recommendation

{{
