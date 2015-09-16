---
title: figure
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Write main content.\nAdd Category, Parent, Children and Compatibility information."
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The figure element (&lt;figure&gt;) represents self-contained content (such as an image), optionally with a caption, that can be referenced as a single unit from the main content of the document.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/figure

---
## Summary

The figure element (&lt;figure&gt;) represents self-contained content (such as an image), optionally with a caption, that can be referenced as a single unit from the main content of the document.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

A figure can be given a caption with the [figcaption](/html/elements/figcaption) element.

## Examples

This example shows the **figure** element to mark up a code listing. The **figcaption** element represents the caption of the figure. The author has also provided a link to the figure in the main content by using a named anchor.

``` html
<!-- Main Content -->
<p>In <a href="#l4">listing 4</a> we see the primary core interface API declaration.</p>
<!-- Figure Content -->
<figure id="l4">
    <figcaption>Listing 4. The primary core interface API declaration.</figcaption>
    <pre><code>interface PrimaryCore {
 boolean verifyDataLine();
 void sendData(in sequence&lt;byte> data);
 void initSelfDestruct();
}</code></pre>
</figure>
```

## Notes

### Remarks

The **figure** element can be used to annotate content that can be referenced from the main content of the document, such as illustrations, diagrams, photos, code listings, and so on. Figures can be moved away from primary content without affecting the flow of the document. You can jump to the figure from the main content by using a named anchor. The [**id**](/html/attributes/id) attribute of the **figure** element specifies the fragment identifier (name of the anchor). The default CSS for the **figure** element is as follows.

    margin: 1em 40px

The **figure** element, like **aside**, separates content from the main flow. Use the **aside** element when the content is simply related, but not essential. Use **figure** if the content is essential, but position is not important. Windows Internet Explorer 9. The **figure** element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-figure-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-figure-element)
:   W3C Recommendation

## See also

### Other articles

-   [figcaption](/html/elements/figcaption)
