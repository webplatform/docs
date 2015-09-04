---
title: tspan
tags:
  - Markup
  - Elements
  - SVG
readiness: 'In Progress'
notes:
  - 'Needs summary, usage, spec reference, standardization status'
uri: svg/elements/tspan

---
# tspan

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, text is modified with [**tSpan**](/svg/elements/text). Each letter has a specified x,y position. Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the modified text.

The text will look like this:



    <!DOCTYPE HTML>
    <html>
      <head></head>
      <body>
        <svg width="400" height="400">
          <text fill="limegreen" font-size="20">
            <tSpan x="50" y="50 55 60 60 60 55 50 45 40 35 30 25 " >
                        SVG forever!</tSpan>
          </text>
        </svg>
      </body>
    </html>

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

You can use the [**x**](/svg/properties/x), [**y**](/svg/properties/y), [**dx**](/svg/properties/dx), [**dy**](/svg/properties/dy), and [**rotate**](/svg/properties/rotate) attributes on the **tspan** element in high-end typography scenarios where individual glyphs require exact placement. You can also use these attributes for minor positioning adjustments between characters or for major positioning adjustments, such as moving the current text position to a new location to achieve the visual effect of a new line of text.

You can create multi-line [**text**](/svg/elements/text) elements by defining different **tspan** elements for each line of text, with [**x**](/svg/properties/x), [**y**](/svg/properties/y), [**dx**](/svg/properties/dx), or [**dy**](/svg/properties/dy) attributes that define the position of each **tspan** element. This setup enables users to select multi-line text selection.

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.4

### Members

The **SVGTSpanElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGTSpanElement** object has these methods:

-   [**getCharNumAtPosition**](/svg/methods/getCharNumAtPosition): Gets the index of the character that the glyph cell bounding box contains at the specified point.
-   [**getComputedTextLength**](/svg/methods/getComputedTextLength): Returns the total sum of all advance values from rendering all characters within the given text element.
-   [**getEndPositionOfChar**](/svg/methods/getEndPositionOfChar): Gets the current text position of the specified character after the character is rendered in the user coordinate system where the glyphs that correspond to the specified character are rendered.
-   [**getExtentOfChar**](/svg/methods/getExtentOfChar): Gets a rectangle that defines the minimum and maximum x-coordinate and y-coordinate values in the user coordinate system where the glyphs that correspond to the specified character are rendered.
-   [**getNumberOfChars**](/svg/methods/getNumberOfChars): Gets the total number of characters that are available for rendering within the current element.
-   [**getRotationOfChar**](/svg/methods/getRotationOfChar): Gets the rotation value of the specified character, relative to the current user coordinate system where the glyphs that corresponding to the specified character are rendered.
-   [**getStartPositionOfChar**](/svg/methods/getStartPositionOfChar): Gets the current text position of the specified character before the character is rendered in the user coordinate system where the glyphs that correspond to the specified character are rendered.
-   [**getSubStringLength**](/svg/methods/getSubStringLength): Calculates the total sum of all advance values from rendering the specified substring of the characters.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.
-   [**selectSubString**](/svg/methods/selectSubString): Selects the specified substring, just as if a user selected the substring interactively.

The **SVGTSpanElement** object has these properties:

-   [**baselineShift**](/svg/attributes/baseline-shift): Sets or retrieves a value that indicates how the dominant baseline should be repositioned relative to the dominant baseline of the parent text content element.
-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**dominantBaseline**](/svg/attributes/dominant-baseline): Sets or retrieves a value that determines or redetermines a scaled-baseline table.
-   [**dx**](/svg/properties/dx): Gets the [**dx**](/svg/properties/dx) attribute on the given element.
-   [**dy**](/svg/properties/dy): Gets the [**dy**](/svg/properties/dy) attribute on the given element.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**fill**](/svg/attributes/fill): Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
-   [**fillOpacity**](/svg/attributes/fill-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
-   [**fillRule**](/svg/attributes/fill-rule): Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**glyphOrientationHorizontal**](/svg/attributes/glyph-orientation-horizontal): Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of horizontal.
-   [**glyphOrientationVertical**](/svg/attributes/glyph-orientation-vertical): Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
-   [**kerning**](/svg/attributes/kerning): Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

Gets or sets a value that indicates whether Metro style app using JavaScript should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

-   [**lengthAdjust**](/svg/properties/lengthAdjust): Gets or sets the [**lengthAdjust**](/svg/properties/lengthAdjust) attribute on the given element.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**rotate**](/svg/properties/rotate): Gets or sets the supplemental character rotation about the current text position.
-   [**stroke**](/svg/attributes/stroke): Sets or retrieves a value that indicates the color to paint along the outline of a given graphical element.
-   [**strokeDasharray**](/svg/attributes/stroke-dasharray): Sets or retrieves one or more values that indicate the pattern of dashes and gaps used to stroke paths.
-   [**strokeDashoffset**](/svg/attributes/stroke-dashoffset): Sets or retrieves a value that specifies the distance into the dash pattern to start the dash.
-   [**strokeLinecap**](/svg/attributes/stroke-linecap): Sets or retrieves a value that specifies the shape to be used at the end of open subpaths when they are stroked.
-   [**strokeLinejoin**](/svg/attributes/stroke-linejoin): Sets or retrieves a value that specifies the shape to be used at the corners of paths or basic shapes when they are stroked.
-   [**strokeMiterlimit**](/svg/attributes/stroke-miterlimit): Sets or retrieves a value that indicates the limit on the ratio of the length of miter joins (as specified in the [**strokeLinejoin**](/svg/attributes/stroke-linejoin) property).
-   [**strokeOpacity**](/svg/attributes/stroke-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to stroke the current object.
-   [**strokeWidth**](/svg/attributes/stroke-width): Sets or retrieves a value that specifies the width of the stroke on the current object.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**textLength**](/svg/properties/textLength): Gets or sets the [**textLength**](/svg/properties/textLength) attribute on the given element.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

