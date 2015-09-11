---
title: xmp
notes:
  - 'Deletion Candidate: Obsolete'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Out of Date'
standardization_status: Deprecated
summary: '(Obsolete) Renders text between the start and end tags without interpreting the HTML in between and using a monospaced font. Non-conforming in HTML5. Use code or pre instead.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/xmp

---
## <span>Summary</span>

(Obsolete) Renders text between the start and end tags without interpreting the HTML in between and using a monospaced font. Non-conforming in HTML5. Use code or pre instead.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

The element is defined as a RAWTEXT element, and has special handling by a text/html parser for legacy reasons.

## <span>Notes</span>

### <span>Remarks</span>

Use of this element is no longer recommended. Use the [pre](/html/elements/pre) or [samp](/html/elements/samp) element instead. HTML elements within an **XMP** element render as text, not as HTML-formatted elements.

## <span>See also</span>

### <span>Other articles</span>

## <span>Use instead</span>

-   [`code`](/html/elements/code)
-   [`pre`](/html/elements/pre)
