---
title: use
tags:
  - Markup
  - Elements
  - SVG
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs summary, usage, spec reference'
code_samples:
  - 'http://gist.github.com/9492902'
uri: svg/elements/use

---
# use

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

Here, the **use** element is used to create three instances of a rectangle defined in a [**defs**](/svg/elements/defs) tag.



    <!DOCTYPE html>
    <html>
        <head></head>
        <body>
            <svg>
                <defs>
                    <rect id="myRect" width="50" height="50" />
                </defs>
                <use x="50" y="50" fill="red" xlink:href="#myRect" />
                <use x="75" y="75" fill="green" xlink:href="#myRect" />
                <use x="100" y="100" fill="blue" xlink:href="#myRect" />
            </svg>
        </body>
    </html>

</pre>
[View live example](http://code.webplatform.org/gist/9492902)

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

For more information, see the [SVG specification](http://go.microsoft.com/fwlink/p/?LinkID=190918).

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.8

### Members

The **SVGUseElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGUseElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGUseElement** object has these properties:

-   [**animatedInstanceRoot**](/svg/properties/animatedInstanceRoot): Gets the animated root of the instance tree of a **use** element.
-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**href**](/svg/properties/href): Gets an **xlink:href** attribute of an element.
-   [**instanceRoot**](/svg/properties/instanceRoot): Gets the root of the instance tree of a **use** element.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**pointerEvents**](/svg/attributes/pointers): Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**transform**](/svg/properties/transform): Gets the value of a [**transform**](/svg/properties/transform) attribute.
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

