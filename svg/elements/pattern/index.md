---
title: pattern
tags:
  - Markup
  - Elements
  - SVG
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Defines a block of graphics which can be used as a repeating pattern tile to paint the fill or stroke of other elements.'
uri: svg/elements/pattern

---
# pattern

## Summary

Defines a block of graphics which can be used as a repeating pattern tile to paint the fill or stroke of other elements.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, a pattern fills a circle. The pattern is made up of a repeated series of wedge-shaped paths. Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the pattern-filled circle.

The pattern-filled circle will look like this:



    <!DOCTYPE HTML>
    <html>
      <head></head>
      <body>
        <!-- Create SVG container. -->
        <svg width="400" height="400">
          <!-- Definitions -->
          <defs>
            <!-- Define pattern for fill. -->
            <pattern id="myPattern" patternUnits="userSpaceOnUse" x="0" y="0" width="30" height="30" >
              <!-- Create path for individual piece of pattern. -->
              <path d="M 0 10 L 25 30 L 50 30 Z" stroke="darkorchid"
                            stroke-width="3" fill="cornflowerblue" />
            </pattern>
          </defs>
          <!-- Circle that will use pattern definition for fill. -->
          <circle cx="100" cy="100" r="75" stroke="forestgreen"
                    stroke-width="3" fill="url(#myPattern)" />
        </svg>
      </body>
    </html>

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

You can use a pattern to fill or stroke an object by using a predefined graphic object that is replicated (that is, tiled) at fixed intervals along the x-axis and y-axis to cover the areas to be painted. You can define a pattern by using a **pattern** element. You can then reference the pattern by the **fill** and **stroke** properties on a given graphics element to specify that the given element is filled or stroked with the referenced pattern.

The [**x**](/svg/properties/x), [**y**](/svg/properties/y), [**width**](/svg/properties/width), [**height**](/svg/properties/height), and [**patternUnits**](/svg/properties/patternUnits) attributes define a reference rectangle somewhere on the infinite SVG canvas. The reference rectangle has its upper-left corner at (**x**, **y**) and its lower-right corner at (**x** + **width**, **y** + **height**). The tiling theoretically extends a series of such rectangles to infinity along the x-axis (positive) and y-axis (negative), with rectangles starting at (**x** + *m* · **width**, y + *n* · **height**) for each possible *m* and *n* integer value.

For more information, see [Scalable Vector Graphics (SVG) 1.0 Specification](http://go.microsoft.com/fwlink/p/?linkid=203737).

### Standards information

-   [Scalable Vector Graphics: Gradients and Patterns](http://go.microsoft.com/fwlink/p/?linkid=199811), Section 13.4.5

### Members

The **SVGPatternElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGPatternElement** object has these methods:

-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.

The **SVGPatternElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**height**](/svg/properties/height): Gets or sets the height of an element.
-   [**href**](/svg/properties/href): Gets an **xlink:href** attribute of an element.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**patternContentUnits**](/svg/properties/patternContentUnits): Gets or sets the [**patternContentUnits**](/svg/properties/patternContentUnits) property on the given **pattern** element, defining the coordinate system for the contents of the **pattern** element.
-   [**patternTransform**](/svg/properties/patternTransform): Gets or sets the definition of an optional transformation from the pattern

coordinate system onto the target coordinate system.

-   [**patternUnits**](/svg/properties/patternUnits): Gets or sets the [**patternUnits**](/svg/properties/patternUnits) property on the given **pattern** element, defining the coordinate system for attributes [**x**](/svg/properties/x), [**y**](/svg/properties/y), [**width**](/svg/properties/width) and [**height**](/svg/properties/height).
-   [**preserveAspectRatio**](/svg/properties/preserveAspectRatio): Gets an XML value that indicates whether to force uniform graphic scaling.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**viewBox**](/svg/properties/viewBox): Gets a value that indicates how a graphic scales to fit a container element.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**width**](/svg/properties/width): Defines the width of an element.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## Related specifications

Specification
:   Status
[SVG 1.1](http://www.w3.org/TR/SVG11/pservers.html#Patterns)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

