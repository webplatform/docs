---
title: 'html comment data-type'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: 'html comment data-type'
  topic: html
notes:
  - 'There is no such thing as a "comment" element. Comments are a part of the HTML syntax. This page should be moved out of the html/elements tree.'
overview_table:
  '[DOM Interface](/dom/interface)': '[Comment](/dom/Comment)'
readiness: 'Not Ready'
summary: "A syntactical production: The comment syntax indicates text within a document that is not displayed on the rendered page in the browser.\nA comment starts with &lt;!-- and ends with --&gt;.\n"
tags:
  - Markup_Elements
  - HTML
uri: 'html/elements/html comment data-type'

---
## Summary

A syntactical production: The comment syntax indicates text within a document that is not displayed on the rendered page in the browser. A comment starts with &lt;!-- and ends with --&gt;.

## Overview Table

[DOM Interface](/dom/interface)
:   [Comment](/dom/Comment)

Comments can contain other HTML elements. Comments do not nest. Start and end tags are required.

In XML mode, comments must not start or end with a dash, and must not contain two consecutive dashes.

## Examples

The following is an example of an **HTML Comment**.

``` html
<!-- This text will not appear in the browser window. -->
```

