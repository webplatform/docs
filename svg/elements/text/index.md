---
title: text
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/text

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## <span>Examples</span>

In the following code example, the text element is used to create a text message in olive 36-point Impact type that reads" Internet Explorer Rocks". Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the text.

It should look like this:

``` html


<!DOCTYPE html>
<html>
    <head></head>
    <body>
        <svg>
            <text x="50" y="50" font-family="Impact" font-size="36" fill="olive">
                SVG Rocks!
            </text>
        </svg>
    </body>
</html>
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The XML character data within the **text** element, along with relevant attributes and properties and character-to-glyph mapping tables within the font itself, define the glyphs to be rendered. The attributes and properties on the **text** element indicate the writing direction, font specification, and painting attributes. These items describe how to render characters.

Because **text** elements are rendered by using the same rendering methods as other graphics elements, all of the same coordinate system transformation, painting, clipping, and masking features that apply to shapes (such as paths and rectangles) also apply to **text** elements.

You can apply a gradient, pattern, clipping path, mask, or filter to text. When you apply one of these items to text and you use **objectBoundingBox** to specify a graphical effect relative to the object bounding box, the units for the object bounding box are computed relative to the entire **text** element in all cases, even when different effects are applied to different [**tSpan**](/svg/elements/tspan) elements within the same **text** element.

The **text** element renders its first glyph (after bidirectionality reordering) at the initial current text position, which is established by the [**x**](/svg/properties/x) and [**y**](/svg/properties/y) attributes on the **text** element. (The attributes might be adjusted because of the value of the **text-anchor** property, the presence of a [**textPath**](/svg/elements/textPath) element that contains the first character, or **x**, **y**, [**dx**](/svg/properties/dx), or [**dy**](/svg/properties/dy) attributes on a [**tSpan**](/svg/elements/tspan), **tref**, or **altGlyph** element that contains the first character.) After the glyphs that corresponds to the given character are rendered, the current text position is updated for the next character. In the simplest case, the new current text position is the previous current text position plus the glyphs' advance value (horizontal or vertical).

### <span>Standards information</span>

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.3

### <span>Members</span>

The **SVGTextElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGTextElement** object has these methods:

-   [**getBBox**](/svg/methods/getBBox): Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
-   [**getCharNumAtPosition**](/svg/methods/getCharNumAtPosition): Gets the index of the character that the glyph cell bounding box contains at the specified point.
-   [**getComputedTextLength**](/svg/methods/getComputedTextLength): Returns the total sum of all advance values from rendering all characters within the given text element.
-   [**getCTM**](/svg/methods/getCTM): Gets the transformation matrix that transforms from the current user units to the viewport coordinate system for the [**nearestViewportElement**](/svg/properties/nearestViewportElement) object.
-   [**getEndPositionOfChar**](/svg/methods/getEndPositionOfChar): Gets the current text position of the specified character after the character is rendered in the user coordinate system where the glyphs that correspond to the specified character are rendered.
-   [**getExtentOfChar**](/svg/methods/getExtentOfChar): Gets a rectangle that defines the minimum and maximum x-coordinate and y-coordinate values in the user coordinate system where the glyphs that correspond to the specified character are rendered.
-   [**getNumberOfChars**](/svg/methods/getNumberOfChars): Gets the total number of characters that are available for rendering within the current element.
-   [**getRotationOfChar**](/svg/methods/getRotationOfChar): Gets the rotation value of the specified character, relative to the current user coordinate system where the glyphs that corresponding to the specified character are rendered.
-   [**getScreenCTM**](/svg/methods/getScreenCTM): Gets the transformation matrix from the current user units to the screen coordinate system.
-   [**getStartPositionOfChar**](/svg/methods/getStartPositionOfChar): Gets the current text position of the specified character before the character is rendered in the user coordinate system where the glyphs that correspond to the specified character are rendered.
-   [**getSubStringLength**](/svg/methods/getSubStringLength): Calculates the total sum of all advance values from rendering the specified substring of the characters.
-   [**getTransformToElement**](/svg/methods/getTransformToElement): Gets the transformation matrix that transforms from the user coordinate system on the current element to the user coordinate system on the specified target element.
-   [**hasExtension**](/svg/methods/hasExtension): Determines if the specified extension is supported.
-   [**selectSubString**](/svg/methods/selectSubString): Selects the specified substring, just as if a user selected the substring interactively.

The **SVGTextElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**dominantBaseline**](/svg/attributes/dominant-baseline): Sets or retrieves a value that determines or redetermines a scaled-baseline table.
-   [**dx**](/svg/properties/dx): Gets the [**dx**](/svg/properties/dx) attribute on the given element.
-   [**dy**](/svg/properties/dy): Gets the [**dy**](/svg/properties/dy) attribute on the given element.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**farthestViewportElement**](/svg/properties/farthestViewportElement): Gets a value that represents the farthest ancestor [**svg**](/svg/elements/svg) element.
-   [**fill**](/svg/attributes/fill): Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
-   [**fillOpacity**](/svg/attributes/fill-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
-   [**fillRule**](/svg/attributes/fill-rule): Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**glyphOrientationHorizontal**](/svg/attributes/glyph-orientation-horizontal): Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of horizontal.
-   [**glyphOrientationVertical**](/svg/attributes/glyph-orientation-vertical): Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
-   [**kerning**](/svg/attributes/kerning): Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

Gets or sets a value that indicates whether the user-agent should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

-   [**lengthAdjust**](/svg/properties/lengthAdjust): Gets or sets the [**lengthAdjust**](/svg/properties/lengthAdjust) attribute on the given element.
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**nearestViewportElement**](/svg/properties/nearestViewportElement): Gets a value that indicates which element established the current viewport.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**pointerEvents**](/svg/attributes/pointers): Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
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
-   [**transform**](/svg/properties/transform): Gets the value of a [**transform**](/svg/properties/transform) attribute.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**x**](/svg/properties/x): Gets or sets the x-coordinate value.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.
-   [**y**](/svg/properties/y): Gets or sets the y-coordinate value.
