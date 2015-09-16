---
title: 'linearGradient'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: linearGradient
  topic: svg
notes:
  - 'Needs summary, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/linearGradient

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, a linear gradient fills a rectangle. The gradient is defined in a definition and fills the rectangle by referencing the gradient. The gradient runs from magenta to cyan.

Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the magenta-to-cyan gradient-filled rectangle.

The gradient-filled rectangle will look like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <!-- Inline SVG -->
    <svg width="400" height="400">
      <defs>
        <!-- Define linear gradient for magenta to cyan. -->
        <linearGradient id="magenta2cyan" >
        <!-- First color is magenta. -->
        <stop offset="0%" style="stop-color:magenta"/>
        <!-- Second color is cyan. -->
        <stop offset="100%" style="stop-color:cyan"/>
        </linearGradient>
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

### Standards information

-   [Scalable Vector Graphics: Gradients and Patterns](http://go.microsoft.com/fwlink/p/?linkid=199811), Section 13.4.2

### Members

The **SVGLinearGradientElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**gradientTransform**](/svg/properties/gradientTransform): Gets a value that contains the definition of an optional, additional transformation from the gradient coordinate system onto the target coordinate system.
-   [**gradientUnits**](/svg/properties/gradientUnits): Gets a value that indicates the type of coordinate system that is used because of a transformation.
-   [**href**](/svg/properties/href): Gets an **xlink:href** attribute of an element.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**spreadMethod**](/svg/properties/spread): Gets a value that determines what happens if a gradient starts or ends inside the bounds of a target rectangle.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**x1**](/svg/properties/x1_(SVGLinearGradientElement)): Gets or sets the x-coordinate for the begining of a gradient vector.
-   [**x2**](/svg/properties/x2_(SVGLinearGradientElement)): Gets or sets the x-coordinate for the end of a gradient vector.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**y1**](/svg/properties/y1_(SVGLinearGradientElement)): Gets or sets the y-coordinate for the begining of a gradient vector.
-   [**y2**](/svg/properties/y2_(SVGLinearGradientElement)): Gets or sets the y-coordinate for the end of a gradient vector.
