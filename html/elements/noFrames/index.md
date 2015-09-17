---
title: 'noFrames'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: noFrames
  topic: html
notes:
  - 'Deletion Candidate: It''s deprecated'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: 'Recognized as a deprecated element. Intended to provide content for browsers that cannot, or are configured not to, display frames.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/noFrames

---
## Summary

Recognized as a deprecated element. Intended to provide content for browsers that cannot, or are configured not to, display frames.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

Deprecated, see [[1]](http://www.w3.org/TR/html5/obsolete.html#non-conforming-features)

## Examples

This example uses the **NOFRAMES** element to specify HTML that is rendered by browsers incapable of displaying frames.

``` html
<FRAMESET>
<NOFRAMES>You need Internet Explorer version 3.0 or later to view
frames!</NOFRAMES>
</FRAMESET>
```

## See also

### Related pages

-   `frame`
