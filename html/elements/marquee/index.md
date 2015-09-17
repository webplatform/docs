---
title: 'marquee'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: marquee
  topic: html
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLMarqueeElement](/dom/HTMLMarqueeElement)'
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: 'Nonstandard. Defines a scrolling area (usually horizontal) of text.'
tags:
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/scrollLeft
    - dom/properties/scrollTop
uri: html/elements/marquee

---
## Summary

Nonstandard. Defines a scrolling area (usually horizontal) of text.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLMarqueeElement](/dom/HTMLMarqueeElement)

No, really. don't use it.

## Notes

### Remarks

The default width of the **MARQUEE** element is equal to the width of its parent element. When a **MARQUEE** is in a **TD** that does not specify a width, you should explicitly set the width of **MARQUEE**. If neither the **MARQUEE** nor the **TD** has a width specified, the marquee is collapsed to a 1-pixel width. To create a vertically scrolling **marquee**, set its [**scrollLeft**](/w/index.php?title=dom/properties/scrollLeft&action=edit&redlink=1) property to 0. To create a horizontally scrolling marquee, set its [**scrollTop**](/w/index.php?title=dom/properties/scrollTop&action=edit&redlink=1) property to 0, overriding any script setting. The [**scrollLeft**](/w/index.php?title=dom/properties/scrollLeft&action=edit&redlink=1) and [**scrollTop**](/w/index.php?title=dom/properties/scrollTop&action=edit&redlink=1) properties are read-only while the **marquee** is scrolling. When not scrolling, **scrollLeft** is read/write for a **marquee** set to scroll horizontally and **scrollTop** is read/write for a **marquee** set to scroll vertically.
