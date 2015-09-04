---
title: figcaption
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - "Examples need \"try it\" link.\nAdd Category, Parent, Children and Compatibility information.\n\nWrite something for main content."
summary: "The figcaption (<figcaption>) defines a caption or legend for a figure element.\nThis element is new in HTML5.\n"
uri: html/elements/figcaption

---
# figcaption

## Summary

The figcaption (\<figcaption\>) defines a caption or legend for a figure element. This element is new in HTML5.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Examples

As the first child of a figure element

``` {.html}

<figure>
  <figcaption>The Stata Center</figcaption>
  <img src="stata.jpg" alt="The Stata Center Building"/>
</figure>
```


    <figure>
      <img src="stata.jpg" alt="The Stata Center Building">
      <figcaption>The Stata Center</figcaption>
    </figure>

## Notes

### Remarks

The first **figcaption** element child of the **figure** element represents the caption of the **figure** element's contents. The **figcaption** element is rendered in place; to move the caption, place it as the first or the last child of the **figure** element. **Note**  If the **figcaption** content provides an adequate text alternative for the visual content in the image, the caption can be used as a text alternative for images in lieu of the [**alt**](/html/attributes/alt) attribute. Windows Internet Explorer 9. The **figcaption** element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-figcaption-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

