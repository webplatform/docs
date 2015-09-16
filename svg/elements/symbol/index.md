---
title: symbol
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, usage, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/symbol

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, a symbol is created and displayed in two different sizes. Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see the symbols.

The symbols will look like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <!-- Create SVG container. -->
    <svg width="400" height="400">
      <!-- Definitions -->
      <defs>
        <!-- Define symbol for fill. -->
        <symbol id="mySymbol" viewBox="0 0 50 50" x="0" y="0" width="10" height="10" >
          <!-- Create path for individual symbol. -->
          <path d="M 0 10 L 25 30 L 50 30 Z" stroke="darkorchid" stroke-width="3" fill="cornflowerblue" />
        </symbol>
      </defs>
      <!-- Insert symbol twice. -->
      <use x="50" y="50" width="50" height="50" xlink:href="#mySymbol" />
      <use x="50" y="100" width="100" height="100" xlink:href="#mySymbol" />
      </svg>
  </body>
</html>
```

</pre>

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Use **symbol** elements for graphics that are used multiple times in the same document to add structure and semantics. Documents that are rich in structure can be rendered graphically, as speech or braille, and promote accessibility.

Compared to a [**g**](/svg/elements/g) element, the **symbol** element itself is not rendered. Only instances of a **symbol** element (that is, a reference to a **symbol** by a [**use**](/svg/elements/use) element) are rendered.

The **symbol** element has [**viewBox**](/svg/properties/viewBox) and [**preserveAspectRatio**](/svg/properties/preserveAspectRatio) attributes that enable a **symbol** to scale-to-fit within a rectangular viewport that the referencing [**use**](/svg/elements/use) element defines.

The [**display**](/css/properties/display) property does not apply to the **symbol** element. Thus, **symbol** elements are not directly rendered even if you set the **display** property to a value other than [**none**](/css/properties/text-decoration-none). **symbol** elements are available for referencing even when you set the **display** property on the **symbol** element or any of its ancestors to **none**.

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.7

### Members

The **SVGSymbolElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGSymbolElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**clipPath**](/svg/properties/clipPath): Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
-   [**externalResourcesRequired**](/svg/properties/externalResourcesRequired): Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**mask**](/svg/attributes/mask): Sets or retrieves a value that indicates a SVG mask.
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**preserveAspectRatio**](/svg/properties/preserveAspectRatio): Gets an XML value that indicates whether to force uniform graphic scaling.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**viewBox**](/svg/properties/viewBox): Gets a value that indicates how a graphic scales to fit a container element.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.

## See also

### Related pages (MSDN)

### Reference

-   [**SVGMarkerElement**](/svg/elements/marker)
-   [**SVGPatternElement**](/svg/elements/patterrn)
