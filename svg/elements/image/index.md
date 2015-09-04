---
title: image
tags:
  - Markup
  - Elements
  - SVG
readiness: 'In Progress'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: svg/elements/image

---
# image

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, two images are displayed on the screen. They are the same image but the size and position are determined by the attributes of the image element.

Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the two images on the screeen.

The images will look like this:



    <!DOCTYPE HTML>
    <html>
      <head></head>
      <body>
        <!-- Create an SVG object. -->
        <svg width="400" height="400">
          <!-- Load an image. -->
          <image x="50" y="50" width="100" height="100"
                    xlink:href="svg.png"/>
          <image x="150" y="150" width="50" height="50"
                    xlink:href="svg.png"/>
        </svg>
      </body>
    </html>

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.11

### Members

The **SVGImageElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGImageElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGImageElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**href**](/svg/properties/href): Gets an **xlink:href** attribute of an element.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**pointerEvents**](/svg/attributes/pointers): Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
-   [**preserveAspectRatio**](/svg/properties/preserveAspectRatio): Gets an XML value that indicates whether to force uniform graphic scaling.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**transform**](/svg/properties/transform): Gets the value of a [**transform**](/svg/properties/transform) attribute.
-   [**viewBox**](/svg/properties/viewBox): Gets a value that indicates how a graphic scales to fit a container element.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

