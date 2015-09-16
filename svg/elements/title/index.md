---
title: title
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/3fe2120a26327b9b9b8e'
notes:
  - 'Needs usage, spec reference, standardization status'
overview_table:
  '[DOM Interface](/dom/interface)': '[SVGElement](/svg/objects/SVGElement)'
readiness: 'In Progress'
summary: 'The title element (&lt;title&gt;) provides a human readable name for container elements and graphics elements.'
tags:
  - Markup
  - Elements
  - SVG
uri: svg/elements/title

---
## Summary

The title element (&lt;title&gt;) provides a human readable name for container elements and graphics elements.

## Overview Table

[DOM Interface](/dom/interface)
:   [SVGElement](/svg/objects/SVGElement)

## Examples

In the following code example, a title element is provided for an ellipse. When you hover over the ellipse, a tooltip may be displayed.

``` html


<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <ellipse cx="150" cy="100" rx="100" ry="75" fill="greenyellow">
        <title>This is the title of an ellipse.</title>
      </ellipse>
    </svg>
  </body>
</html>
```

</pre>
[View live example](http://code.webplatform.org/gist/3fe2120a26327b9b9b8e)

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Each container element or graphics element in a Scalable Vector Graphics (SVG) drawing can provide a [**desc**](/svg/elements/desc) or a **title** textual description. The **title** elements are not rendered as part of the graphics. Instead, they appear as a tooltip as the the pointer moves over particular elements in the drawing.

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.6

### Members

The **SVGTitleElement** object has these properties:

-   [**className**](/svg/properties/className): Gets the names of the classes that are assigned to this object.
-   [**focusable**](/svg/properties/focusable): Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when a user presses the Tab key).
-   [**ownerSVGElement**](/svg/properties/ownerSVGElement): Gets the nearest ancestor [**svg**](/svg/objects/SVGElement) element.
-   [**style**](/svg/properties/style): Gets a [**style**](/css/cssom/style) object.
-   [**viewportElement**](/svg/properties/viewportElement): Gets the element that established the current viewport.
-   [**xmlbase**](/svg/properties/xmlbase): Gets or sets the **base** attribute on the element.
-   [**xmllang**](/svg/properties/xmllang): Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
-   [**xmlspace**](/svg/properties/xmlspace): Gets or sets a value that indicates whether white space is preserved in character data.

## See also

### Related pages

-   [**SVGDescElement**](/svg/elements/desc)
