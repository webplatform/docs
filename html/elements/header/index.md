---
title: header
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add Category, Parent and Children information. Complete Compatibility information.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
summary: 'The header element (&lt;header&gt;) represents the header of a section: a group of introductory or navigational aids.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/header

---
## Summary

The header element (&lt;header&gt;) represents the header of a section: a group of introductory or navigational aids.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

The **header** element represents introductory content for its nearest ancestor sectioning content ([article](/html/elements/article) [aside](/html/elements/aside) [nav](/html/elements/nav) [section](/html/elements/section)) or sectioning root element ([blockquote](/html/elements/blockquote) [body](/html/elements/body) [fieldset](/html/elements/fieldset) [figure](/html/elements/figure) [td](/html/elements/td)).

A header element is intended to usually contain the section's heading (an h1–h6 element or an hgroup element), but this is not required. The header element can also be used to wrap a section's table of contents, a search form, or any relevant logos.

## Examples

The following snippet shows how the element can be used to mark up a specification's header

``` html

<header>
 <hgroup>
  <h1>Scalable Vector Graphics (SVG) 1.2</h1>
  <h2>W3C Working Draft 27 October 2004</h2>
 </hgroup>
 <dl>
  <dt>This version:</dt>
  <dd><a href="http://www.w3.org/TR/2004/WD-SVG12-20041027/">http://www.w3.org/TR/2004/WD-SVG12-20041027/</a></dd>
  <dt>Previous version:</dt>
  <dd><a href="http://www.w3.org/TR/2004/WD-SVG12-20040510/">http://www.w3.org/TR/2004/WD-SVG12-20040510/</a></dd>
  <dt>Latest version of SVG 1.2:</dt>
  <dd><a href="http://www.w3.org/TR/SVG12/">http://www.w3.org/TR/SVG12/</a></dd>
  <dt>Latest SVG Recommendation:</dt>
  <dd><a href="http://www.w3.org/TR/SVG/">http://www.w3.org/TR/SVG/</a></dd>
  <dt>Editor:</dt>
  <dd>Dean Jackson, W3C, <a href="mailto:dean@w3.org">dean@w3.org</a></dd>
  <dt>Authors:</dt>
  <dd>See <a href="#authors">Author List</a></dd>
 </dl>
 <p class="copyright"><a href="http://www.w3.org/Consortium/Legal/ipr-notic ...
</header>

```

In this example, the page has a page heading given by the h1 element, and two subsections whose headings are given by h2 elements. The content after the header element is still part of the last subsection started in the header element, because the header element doesn't take part in the outline algorithm

``` html

<body>
 <header>
  <h1>Little Green Guys With Guns</h1>
  <nav>
   <ul>
    <li><a href="/games">Games</a>
    <li><a href="/forum">Forum</a>
    <li><a href="/download">Download</a>
   </ul>
  </nav>
  <h2>Important News</h2> <!-- this starts a second subsection -->
  <!-- this is part of the subsection entitled "Important News" -->
  <p>To play today's games you will need to update your client.</p>
  <h2>Games</h2> <!-- this starts a third subsection -->
 </header>
 <p>You have three active games:</p>
 <!-- this is still part of the subsection entitled "Games" -->
 ...

```

## Notes

### Remarks

Windows Internet Explorer 9. The **header** element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility. A **header** element can contain the section's heading (an **h1-h6** element or an **hgroup** element) but this is not required. The **header** element can also be used to wrap a section's table of contents, a search form, or any relevant logos. The **header** element is not sectioning content; it does not introduce a new section.

### HTML information

||
|Closing Tag|required|
|CSS Display|block|

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-header-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/sections.html#the-header-element)
:   W3C Recommendation

## See also

### External resources

<http://www.w3.org/TR/html-markup/header.html>
