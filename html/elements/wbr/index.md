---
title: wbr
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/wbr)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Add summary, notes, compatibility.\nAdd information about alternatives for producing word breaks, including Unicode zero-width spaces."
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'The Word Break Opportunity (wbr) element represents a position within text where the browser may optionally break a line, though its line-breaking rules would not otherwise create a break at that location.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/wbr

---
## Summary

The Word Break Opportunity (wbr) element represents a position within text where the browser may optionally break a line, though its line-breaking rules would not otherwise create a break at that location.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Examples

This example uses the **WBR** element to create line breaks. In contrast, the **NOBR** element does not break lines.

``` html
<NOBR>This line of text will not break, no matter how narrow the window gets.</NOBR>
<NOBR>This one, however,<WBR> will break after the word "however,"
if the window gets small enough.</NOBR>
```

## Notes

### Remarks

A soft line break is a point inside a **NOBR** section at which a line break is permitted but not required.

On UTF-8 encoded pages, behaves like the U+200B ZERO-WIDTH SPACE code point. In particular, it behaves like a Unicode bidi BN code point, meaning it has no effect on bidi-ordering:

123,<wbr></wbr>456

displays, when not broken on two lines, 123,456 and not 456,123.

For the same reason, the \<﻿wbr﻿\> element does not introduce a hyphen at the line break point. To make a hyphen appear only at the end of a line, use the soft hyphen character entity (&﻿shy;) instead.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-wbr-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-wbr-element)
:   W3C Recommendation

## See also

### Related pages (MSDN)

-   `br`
