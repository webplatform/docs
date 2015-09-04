---
title: etextContent
tags:
  - Markup
  - Elements
  - SVG
readiness: 'Not Ready'
notes:
  - 'Needs properly flagged and automatically collected children instead of manual links, summary, spec reference, standardization status'
uri: svg/elements/etextContent

---
# etextContent

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.1

### Members

The **SVGTextContentElement** object has these methods:

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

The **SVGTextContentElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**lengthAdjust**](/svg/properties/lengthAdjust): Gets or sets the [**lengthAdjust**](/svg/properties/lengthAdjust) attribute on the given element.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**requiredExtensions**](/svg/properties/requiredExtensions): Gets a white space-delimited list of required language extensions.
-   [**requiredFeatures**](/svg/properties/requiredFeatures): Gets or sets a white space-delimited list of feature strings.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**systemLanguage**](/svg/properties/systemLanguage): Gets or sets a comma-separated list of language names.
-   [**textLength**](/svg/properties/textLength): Gets or sets the [**textLength**](/svg/properties/textLength) attribute on the given element.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

