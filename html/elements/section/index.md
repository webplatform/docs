---
title: section
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines sections in a document, such as chapters, headers, footers, or any other sections of the document. It is new to HTML5.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/section

---
## Summary

Defines sections in a document, such as chapters, headers, footers, or any other sections of the document. It is new to HTML5.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

A section is a thematic grouping of content, typically with a heading. Examples of sections would be chapters, the various tabbed pages in a tabbed dialog box, or the numbered sections of a thesis. A website's home page could be split into sections for an introduction, news items, and contact information. The **section** element is not a generic container element. Authors are encouraged to use the **div** element for styling purposes or when an element is needed as a convenience for scripting. The **section** element is appropriate only if the element's contents would be listed explicitly in the document's outline.

## Examples

In the following example, an **article** (part of a larger document about apples) contains two short sections.

``` html
<article>
 <hgroup>
  <h1>Apples</h1>
  <h2>Tasty, delicious fruit!</h2>
 </hgroup>
 <p>The apple is the pomaceous fruit of the apple tree.</p>
 <section>
  <h1>Red Delicious</h1>
  <p>These bright red apples are the most common found in many
  supermarkets.</p>
 </section>
 <section>
  <h1>Granny Smith</h1>
  <p>These juicy, green apples make a great filling for
  apple pies.</p>
 </section>
</article>
```

The rank of **h1-h6** elements is determined by the number in their name. The **h1** element is said to have the highest rank; the **h6** element has the lowest rank. Two elements with the same name have the same rank. The default style applied to **hn** elements varies according to the rank of the element. However, the rank of headings that appear within a **section** element is automatically reduced. This affects the visual appearance of the headings inside the **section** element. In the following example, the author uses **h1** elements without worrying whether a particular section is at the top level, the second level, the third level, and so on. The two outlines produce equivalent output.

``` html
<!-- First outline -->
<h1>Let's call it a draw(ing surface)</h1>
<h2>Diving in</h2>
<h2>Simple shapes</h2>
<h2>Canvas coordinates</h2>
<h3>Canvas coordinates diagram</h3>
<h2>Paths</h2>
<hr/>
<!-- Equivalent outline using section elements -->
<h1>Let's call it a draw(ing surface)</h1>
<section>
<h1>Diving in</h1>
</section>
<section>
<h1>Simple shapes</h1>
</section>
<section>
<h1>Canvas coordinates</h1>
<section>
<h1>Canvas coordinates diagram</h1>
</section>
</section>
<section>
<h1>Paths</h1>
</section>
```

## Usage

     Note  Authors are encouraged to use the article element instead of the section element when it would make sense to syndicate the contents of the element.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-section-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/sections.html#the-section-element)
:   W3C Recommendation

## See also

### Related articles

#### Document Structure

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [main](/html/elements/main)

-   [nav](/html/elements/nav)

-   [p](/html/elements/p)

-   **section**
