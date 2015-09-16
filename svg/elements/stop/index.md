---
title: 'stop'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: stop
  topic: svg
notes:
  - 'Needs summary, example, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/stop

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

**Needs Examples**: This section should include examples.

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

You must define two **stop** elements to create a gradient effect. If no **stop** elements, painting occurs as if you specify **none** as the paint style. If you define one **stop** element, the paint occurs by using a solid-color fill with the color that is defined for that gradient **stop** element.

### Standards information

-   [Scalable Vector Graphics: Gradients and Patterns](http://go.microsoft.com/fwlink/p/?linkid=199811), Section 13.4.4

### Members

The **SVGStopElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGStopElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**offset**](/svg/properties/offset): Gets or sets a value that indicates where the gradient stop is placed within the gradient.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**stopColor**](/svg/attributes/stop-color): Sets or retrieves a value that indicates what color to use at the current gradient stop.
-   [**stopOpacity**](/svg/attributes/stop-opacity): Sets or retrieves a value that defines the opacity of the current gradient stop.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.

## See also

### Related pages

### Reference

-   [**SVGLinearGradientElement**](/svg/elements/linearGradient)
-   [**SVGRadialGradientElement**](/svg/elements/radialGradient)
