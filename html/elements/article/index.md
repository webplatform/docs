---
title: 'article'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: article
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The article element (&lt;article&gt;) defines a self-contained composition within a page.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/article

---
## Summary

The article element (&lt;article&gt;) defines a self-contained composition within a page.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

"Article" is an element, first introduced in HTML5, for the purpose of relieving "div" fatigue and overuse. An **article** element might represent content like a:

-   forum post
-   magazine or newspaper article
-   blog entry
-   user-submitted comment
-   interactive widget or gadget

or any other independent item of content.

When **article** elements are nested, the inner article should be related to the contents of the outer article. For example, a blog entry on a site that accepts user-submitted comments might represent the comments as **article** elements nested within the **article** element for the blog entry.

## Examples

The following example shows the basic structure of an article using **article**, **header**, and **footer** elements.

``` html
<article>
 <header>
  <h1>Article Heading</h1>
 </header>
 <p>Article Text</p>
 <p>...</p>
 <footer>Article Footer</footer>
</article>
```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-article-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/sections.html#the-article-element)
:   W3C Recommendation

## See also

### Other articles

[nav](/html/elements/nav) - The HTML navigation element is often used as a child element of the article tag.

### External resources

-   <http://www.w3.org/TR/html-markup/article.html#article>
