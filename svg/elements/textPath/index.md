---
title: textPath
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
uri: svg/elements/textPath

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## <span>Examples</span>

In the following code example, the **textPath** element is used to define a path for text rendering. The same path is used in the [**path**](/svg/elements/path) example. Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the text on a path.

It should look like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <defs>
        <path id="myTextPath" d="M 50,100 Q 150,50 250,100" />
      </defs>
      <text fill="steelblue" font-size="20">
        <textPath xlink:href="#myTextPath">Internet Explorer Forever!</textPath>
      </text>
    </svg>
  </body>
</html>
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

In addition to text that is drawn in a straight line, you can also place text along the shape of a [**path**](/svg/elements/path) element in SVG. To render a block of text along the shape of a **path** element, include the given text within a **textPath** element that includes an **xlink:href** attribute with an Internationalized Resource Identifier (IRI) reference to the **path** element.

### <span>Standards information</span>

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.6

### <span>Members</span>

The **SVGTextPathElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGTextPathElement** object has these methods:

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

The **SVGTextPathElement** object has these properties:

-   [**baselineShift**](/svg/attributes/baseline-shift): Sets or retrieves a value that indicates how the dominant baseline should be repositioned relative to the dominant baseline of the parent text content element.
-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**dominantBaseline**](/svg/attributes/dominant-baseline): Sets or retrieves a value that determines or redetermines a scaled-baseline table.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**fill**](/svg/attributes/fill): Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
-   [**fillOpacity**](/svg/attributes/fill-opacity): Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
-   [**fillRule**](/svg/attributes/fill-rule): Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**glyphOrientationHorizontal**](/svg/attributes/glyph-orientation-horizontal): Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of horizontal.
-   [**glyphOrientationVertical**](/svg/attributes/glyph-orientation-vertical): Sets or retrieves a value that alters the orientation of a sequence of characters relative to an inline-progression-direction of vertical.
-   [**href**](/svg/properties/href): Gets an **xlink:href** attribute of an element.
-   [**kerning**](/svg/attributes/kerning): Gets or sets a value that indicates whether Internet Explorer should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

Gets or sets a value that indicates whether Metro style app using JavaScript should adjust inter-glyph spacing based on kerning tables that are included in the relevant font (that is, enable auto-kerning) or instead disable auto-kerning and set inter-character spacing to a specific length (typically zero).

-   [**lengthAdjust**](/svg/properties/lengthAdjust): Gets or sets the [**lengthAdjust**](/svg/properties/lengthAdjust) attribute on the given element.
