---
title: desc
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The desc element (&lt;desc&gt;) provides a human readable description for container elements and graphics elements.'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/desc

---
## <span>Summary</span>

The desc element (&lt;desc&gt;) provides a human readable description for container elements and graphics elements.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## <span>Examples</span>

In the following code example, the **desc** element is used to define a description of an element. This element can be read programatically to analyze SVG structure.

Copy this sample to a text file and save it with the *.html* file extension. Run it in Internet Explorer 9 to see a greenyellow ellipse.

The element will look like this:

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <ellipse cx="150" cy="100" rx="100" ry="75" fill="greenyellow">
        <desc>This is the description of an ellipse.</desc>
      </ellipse>
    </svg>
  </body>
</html>
```

</pre>

## <span>Notes</span>

### <span>Remarks</span>

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

### <span>Standards information</span>

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.5

### <span>Members</span>

The **SVGDescElement** object has these events:

-   [**onload**](/svg/events/load): Occurs when the browser has fully parsed the element and all of its descendants.

The **SVGDescElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.

## <span>Related specifications</span>

[SVG 1.1](http://www.w3.org/TR/SVG/struct.html#DescriptionAndTitleElements)
:   W3C Recommendation

[SVG Tiny 1.2](http://www.w3.org/TR/SVGTiny12/struct.html#TitleAndDescriptionElements)
:   W3C Recommendation
