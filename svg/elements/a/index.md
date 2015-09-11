---
title: a
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'Almost Ready'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/a

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## <span>Examples</span>

In the following code example, the a element is used to create a hyperlink using the xlink namespace. The link is attached to the circle element inside an inline SVG element.

Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 and click on the chocolate circle.

It should look like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <!-- Create an SVG object -->
    <svg width="400" height="400">
        <!-- Create a link. -->
        <a xlink:href="http://msdn.microsoft.com/en-us/ie/">
          <!-- Create a circle. -->
          <circle cx="100" cy="100" r="50" fill="chocolate"/>
          </circle>
        </a>
    </svg>
  </body>
</html>
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

SVG provides an **a** element to indicate links (also known as hyperlinks or web links). The **a** element may contain any element that its parent may contain, except itself.

SVG uses XLink for all link definitions (that is, **xmlns:xlink="<http://www.w3.org/1999/xlink>"** must be present in the containing [**svg**](/svg/elements/svg) element). Each link associates exactly two resources, one local and one remote, going from the former to the latter.

A link is defined for each separate rendered element contained within the **a** element; thus, if the **a** element contains three [**circle**](/svg/elements/circle) elements, a link is created for each circle. For each rendered element within an **a** element, the given rendered element is the local resource (the source anchor for the link).

The remote resource (the destination for the link) is defined by a URL (technically a [<http://go.microsoft.com/fwlink/p/?linkid=203507> W3C IRI]) specified by the XLink (that is, **xlink:href** attribute) on the **a** element. The remote resource may be any web resource (for example, an image, a video clip, a sound bite, a program, another SVG document, an HTML document, an element within the current document, an element within a different document, etc.). By activating these links (by clicking with the mouse, through keyboard input, by voice commands, etc.), users may visit these resources.

### <span>Standards information</span>

-   [Scalable Vector Graphics: Linking](http://go.microsoft.com/fwlink/p/?linkid=199815), Section 17.4.1

### <span>Members</span>

The **SVGAElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGAElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGAElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**href**](/svg/properties/href): Gets an **xlink:href** attribute of an element.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**target**](/svg/properties/target): Specifies where to open a linked document.
-   [**transform**](/svg/properties/transform): Gets the value of a [**transform**](/svg/properties/transform) attribute.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
