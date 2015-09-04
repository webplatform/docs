---
title: nav
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Add Category, Parent and Children information. Complete Compatibility table.'
summary: 'The HTML Navigation Element (<nav>) represents a section of navigation links: a page that links to other pages, or to parts within the page'
uri: html/elements/nav

---
# nav

## Summary

The HTML Navigation Element (\<nav\>) represents a section of navigation links: a page that links to other pages, or to parts within the page

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Examples

The following example uses the **nav** element to indicate that a list contains site navigation links.

``` {.html}
<nav>
 <h1>Site Navigation</h1>
 <ul>
  <li><a href="index.html">Home</a></li>
  <li><a href="gallery.html">Photo</a></li>
  <li><a href="news.html">Updates</a></li>
 </ul>
</nav>
```

## Usage

     Not all groups of links on a document need to be in a nav element, only sections that consist of major navigation blocks. In particular, it is common for footer elements to have a short list of links to various documents of a site, such as the terms of service, home, and copyright. The footer element alone is sufficient for such cases, and does not require a nav element.

**Note** Some devices and applications (such as screen readers) might use the **nav** element as a way to determine what content on the document to initially skip or provide on request.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-nav-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/sections.html#the-nav-element)
:   W3C Recommendation

## See also

### Related articles

#### Document Structure

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [main](/html/elements/main)

-   **nav**

-   [p](/html/elements/p)

-   [section](/html/elements/section)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

