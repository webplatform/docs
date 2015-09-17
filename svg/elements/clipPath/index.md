---
title: 'clipPath'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: clipPath
  topic: svg
notes:
  - 'Needs summary, example, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup_Elements
  - SVG
  - Needs_Summary
uri: svg/elements/clipPath

---
## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, the clipPath element is used to create a clipping path that will visually hide part of an element. The clipping path is defined by a circle in a defs element and has a defined URL.

``` xml
<path d="M 50,100 Q 150,50 250,100" stroke="hotpink"
    stroke-width="10" fill="white"/>
```

 The original path would have looked like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <path d="M 50,100 Q 150,50 250,100" stroke="hotpink"
          stroke-width="10" fill="white" />
    </svg>
  </body>
</html>
```

</pre>

The path after being clipped by the circle looks like this:

``` xml
<svg width="400" height="400">
  <defs>
    <clipPath id="myClipPath">
      <circle cx=100 cy=100 r=50 />
    </clipPath>
  </defs>
  <path d="M 50,100 Q 150,50 250,100" stroke="hotpink"
      stroke-width="10" fill="white" clip-path="url(#myClipPath)"/>
</svg>
```

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <defs>
        <clipPath id="myClipPath">
          <circle cx=100 cy=100 r=50 />
        </clipPath>
      </defs>
      <path d="M 50,100 Q 150,50 250,100" stroke="hotpink"
         stroke-width="10" fill="white" clip-path="url(#myClipPath)"/>
    </svg>
  </body>
</html>
```

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

### Standards information

-   [Scalable Vector Graphics: Clipping, Masking and Compositing](http://go.microsoft.com/fwlink/p/?linkid=199810), Section 14.6.1

### Members

The **SVGClipPathElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGClipPathElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGClipPathElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPathUnits**](/svg/properties/clipPathUnits): Gets or sets the given **SVGClipPathElement** element.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**transform**](/svg/properties/transform): Gets the value of a [**transform**](/svg/properties/transform) attribute.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
