---
title: 'radialGradient'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: radialGradient
  topic: svg
notes:
  - 'Needs summary, usage, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup_Elements
  - SVG
  - Needs_Summary
uri: svg/elements/radialGradient

---
## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, a radial gradient fills a rectangle. The gradient is defined in a definition and fills the rectangle by referencing the gradient. The gradient runs from magenta to cyan, starting in the center with magenta and working outward to cyan.

Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the circular magenta to cyan gradient filling the rectangle.

The radial-filled rectangle will look like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <!-- Inline SVG -->
    <svg width="400" height="400">
      <defs>
        <!-- Define radial gradient for magenta to cyan. -->
        <radialGradient id="magenta2cyan" >
        <!-- First color is magenta. -->
        <stop offset="0%" style="stop-color:magenta"/>
        <!-- Second color is cyan. -->
        <stop offset="100%" style="stop-color:cyan"/>
        </radialGradient>
      </defs>
      <!-- Rectangle fill is defined by linear gradient in defs. -->
      <rect width="100" height="50" x="50" y="50" style="fill:url(#magenta2cyan)"/>
    </svg>
  </body>
</html>
```

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The **radialGradient** element inherits properties from its ancestors instead of from the element that references the **radialGradient** element. **radialGradient** elements are never rendered directly. They exist so that you can reference them by using the **fill** and **stroke** properties.

The **display** property does not apply to the **radialGradient** element. **radialGradient** elements are not directly rendered even if the **display** property is set to a value other than **none**. But **radialGradient** elements are available for referencing even when the **display** property on the **radialGradient** element or any of its ancestors is set to **none**.

### Standards information

-   [Scalable Vector Graphics: Gradients and Patterns](http://go.microsoft.com/fwlink/p/?linkid=199811), Section 13.4.3

### Members

The **SVGRadialGradientElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**cx**](/svg/properties/cx_(SVGRadialGradientElement)): Gets or sets the x-coordinate for the center of the largest (that is, outermost) circle of a radial gradient.
-   [**cy**](/svg/properties/cy_(SVGRadialGradientElement)): Gets or sets the y-coordinate for the center of the largest (that is, outermost) circle of a radial gradient.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**fx**](/svg/properties/fx): Gets or sets the x-coordinate for the focal point of a radial gradient.
-   [**fy**](/svg/properties/fy): Gets or sets the y-coordinate for the focal point of a radial gradient.
-   [**gradientTransform**](/svg/properties/gradientTransform): Gets a value that contains the definition of an optional, additional transformation from the gradient coordinate system onto the target coordinate system.
-   [**gradientUnits**](/svg/properties/gradientUnits): Gets a value that indicates the type of coordinate system that is used because of a transformation.
-   [**href**](/svg/properties/href): Gets an **xlink:href** attribute of an element.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**r**](/svg/properties/r_(SVGRadialGradientElement)): Gets or sets the radius of a radial gradient.
-   [**spreadMethod**](/svg/properties/spread): Gets a value that determines what happens if a gradient starts or ends inside the bounds of a target rectangle.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
