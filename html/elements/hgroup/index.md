---
title: 'hgroup'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: hgroup
  topic: html
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: '(Obsolete) The hgroup element (&lt;hgroup&gt;) is typically used to group a set of one or more h1-h6 elements — to group, for example, a section title and an accompanying subtitle. The hgroup element (&lt;hgroup&gt;) element is obsolete in HTML5.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/hgroup

---
## Summary

(Obsolete) The hgroup element (&lt;hgroup&gt;) is typically used to group a set of one or more h1-h6 elements — to group, for example, a section title and an accompanying subtitle. The hgroup element (&lt;hgroup&gt;) element is obsolete in HTML5.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Obsolete

The hgroup element is obsolete in HTML. Consider the [header](/html/elements/header) element, or a `<span class="subheading">` element with differentiated styling.

## Point

-   The element is used to group a set of h1–h6 elements when the heading has multiple levels, such as subheadings, alternative titles, or taglines. [[Example A]](#Example_A)
-   For the purposes of document summaries, outlines, and the like, the text of hgroup elements is defined to be the text of the highest ranked h1–h6 element descendant of the hgroup element, if there are any such elements, and the first such element if there are multiple elements with that rank.
-   The rank of an hgroup element is the rank of the highest-ranked h1–h6 element descendant of the hgroup element, if there are any such elements, or otherwise the same as for an h1 element (the highest rank).

## Examples

The following is an example of a valid heading. The **hgroup** masks the **h2** element (which acts as a secondary title) from the outline algorithm.

``` html
<hgroup>
 <h1>Dr. Strangelove</h1>
 <h2>Or: How I Learned to Stop Worrying and Love the Bomb</h2>
</hgroup>
```

For document summaries and outlines, the text of **hgroup** elements is defined as the text of the highest ranked **h1-h6** element descendant, or the first such element if there are multiple elements with the highest rank. If there are no such elements, then the text of the **hgroup** element is the empty string. The following script demonstrates how to implement this behavior.

``` js
function findHeadings(node)
{
    // First check if this node has an <hgroup>.
    var hg = node.getElementsByTagName("HGROUP");
    if(hg.length>0)
        node = hg[0];
    // Now find the highest ranking heading.
    var ranks = [ "H1","H2","H3","H4","H5","H6" ];
    for (var i=0; i<ranks.length; i++) {
        var headings = node.getElementsByTagName(ranks[i]);
        if(headings.length>0)
            return headings[0].textContent;
    }
    // No headings present, return empty string.
    return "";
}
```

## Notes

### Remarks

Windows Internet Explorer 9. The **hgroup** element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility. The **hgroup** element is used to group a set of **h1-h6** elements when the heading has multiple levels, such as subheadings, alternative titles, or taglines. Other elements of heading content in the **hgroup** element indicate subheadings or subtitles.

## See also

### External resources

<http://www.w3.org/html/wg/drafts/html/CR/obsolete.html#hgroup>

### Related pages

-   `Reference`
-   `article`
-   `aside`
-   `figcaption`
-   `figure`
-   `footer`
-   `header`
-   `mark`
-   `nav`
-   `section`
