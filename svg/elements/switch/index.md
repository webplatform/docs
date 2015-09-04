---
title: switch
tags:
  - Markup
  - Elements
  - SVG
readiness: 'In Progress'
notes:
  - 'Needs summary, usage, spec reference, standardization status'
uri: svg/elements/switch

---
# switch

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

The following code example uses the **switch** element to provide a graphical representation of a paragraph if XMHTML is not supported.



    <?xml version="1.0" standalone="yes"?>
    <svg width="4in" height="3in" version="1.1"
     xmlns = 'http://www.w3.org/2000/svg'>
      <!-- The <switch> element will process the first child element
           whose testing attributes evaluate to TRUE.-->
      <switch>
        <!-- Process the embedded XHTML if the requiredExtensions attribute
             evaluates to TRUE (that is, the browser supports XHTML
             embedded within SVG). -->
        <foreignObject width="100" height="50"
                       requiredExtensions="http://example.com/SVGExtensions/EmbeddedXHTML">
          <!-- XHTML content goes here -->
          <body xmlns="http://www.w3.org/1999/xhtml">
            <p>Here is a paragraph that requires word wrap.</p>
          </body>
        </foreignObject>
        <!-- ELSE, process the following alternate SVG.
             Note that there are no testing attributes on the <text> element.
             If no testing attributes are provided, it is as if there
             were testing attributes and they evaluated to TRUE.-->
        <text font-size="10" font-family="Verdana">
          <tspan x="10" y="10">Here is a paragraph that</tspan>
          <tspan x="10" y="20">requires word wrap.</tspan>
        </text>
      </switch>
    </svg>

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The **switch** element evaluates the [**requiredFeatures**](/svg/properties/requiredFeatures), [**requiredExtensions**](/svg/properties/requiredExtensions), and [**systemLanguage**](/svg/properties/systemLanguage) attributes on its direct child elements in order, and then processes and renders the first child element that these attributes evaluate to TRUE for. All other child elements are skipped and not rendered. If the child element is a container element (such as an [**g**](/svg/elements/g) element), the entire subtree is processed and rendered or skipped and not rendered.

The values of the [**display**](/css/properties/display) and [**visibility**](/css/properties/visibility) properties does not affect the **switch** element processing. In particular, if you set **display** to [**none**](/css/properties/text-decoration-none) on a child element of a **switch** element, it does not affect TRUE and FALSE testing that is associated with processing **switch** elements.

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.13

### Members

The **SVGSwitchElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGSwitchElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGSwitchElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

