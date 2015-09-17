---
title: 'view'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: view
  topic: svg
notes:
  - 'Needs summary, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup_Elements
  - SVG
  - Needs_Summary
uri: svg/elements/view

---
## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

The following code example shows how to zoom in and zoom out of rendered content.

``` html


<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<!-- 400 pixels per 100 user units, or 4 pixels per 1 user unit. -->
<svg width="400px" height="400px" viewBox="0 0 100 100" version="1.1" xmlns="http://www.w3.org/2000/svg"
     xmlns:xlink="http://www.w3.org/1999/xlink">  <!-- Required for 'xlink' usage. -->
  <title>The SVG view Element</title>
  <desc>
        The key concept is that the 'viewBox' attribute values of the
        associated 'view' element are essentially applied to the 'viewBox'
        attributes of its parent 'svg' element.
  </desc>
  <defs>
    <radialGradient id="myRadialGradient">
      <stop offset="0%" stop-color="yellow" />
      <stop offset="50%" stop-color="white" />
      <stop offset="100%" stop-color="blue" />
    </radialGradient>
  </defs>
  <view id="normalView" viewBox="0 0 100 100"/>  <!-- Same 'viewBox' values as on the 'svg' element (that is, 4 pixels per user unit). -->
  <view id="halfView"   viewBox="0 0 200 200"/>  <!-- 400 pixels per 200 user units, or 2 pixels per 1 user unit - shrinking things. -->
  <view id="doubleView" viewBox="0 0  50  50"/>  <!-- 400 pixels per 50 user units, or 8 pixels per 1 user unit - expanding things. -->
  <!-- Outline the initial viewport. -->
  <rect x="0" y="0" width="100%" height="100%" style="stroke: green; fill: none;"/>
  <!-- Fill the viewport with something interesting. -->
  <circle fill="url(#myRadialGradient)" stroke="black" stroke-width="1" cx="50" cy="50" r="40"/>
  <!-- Provide the user with a way, by clicking the links, to essentially change the 'svg' element's 'viewBox' values. -->
  <a xlink:href="#doubleView">
    <text x="2" y="6" font-size="5">[double size]</text>
  </a>
  <a xlink:href="#normalView">
    <text x="39" y="6" font-size="5">[normal size]</text>
  </a>
  <a xlink:href="#halfView">
    <text x="77" y="6" font-size="5">[half size]</text>
  </a>
</svg>
```

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The **view** element can change the [**viewBox**](/svg/properties/viewBox) attributes of its parent [**svg**](/svg/elements/svg) element. For example, you can use this behavior to zoom in or zoom out of rendered SVG content.

### Standards information

-   [Scalable Vector Graphics: Linking](http://go.microsoft.com/fwlink/p/?linkid=199815), Section 17.4.2

### Members

The **SVGViewElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGViewElement** object has these properties:

-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**preserveAspectRatio**](/svg/properties/preserveAspectRatio): Gets an XML value that indicates whether to force uniform graphic scaling.
-   [**viewBox**](/svg/properties/viewBox): Gets a value that indicates how a graphic scales to fit a container element.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**viewTarget**](/svg/properties/viewTarget): Gets the [**viewTarget**](/svg/properties/viewTarget) attribute of a **view** element.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**zoomAndPan**](/svg/properties/zoomAndPan): Gets the [**zoomAndPan**](/svg/properties/zoomAndPan) attribute of an element.
