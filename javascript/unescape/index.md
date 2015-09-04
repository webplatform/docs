---
title: unescape
tags:
  0: JS
  1: Basic
  3: Function
readiness: 'Not Ready'
notes:
  - 'Deletion candidate; deprecated function'
summary: "Deprecated\n"
uri: javascript/unescape

---
# unescape

## Summary

Deprecated

The deprecated **unescape()** function decodes a string that is usually encoded with the **escape** function.

## Syntax

    unescape(str)

**str**
:   Required. A String to be decoded

## Examples

``` {.js}
unescape("webplatform"); // "webplatform"
unescape("%FCmlaut"); // "ümlaut"
unescape("%u65E5%u672C%u8A9E"); // "日本語"
```

## Remarks

All characters encoded with the % xx hexadecimal form are replaced by their ASCII character set equivalents.

Characters encoded in **%u** xxxx format (Unicode characters) are replaced with the Unicode character with hexadecimal encoding xxxx.

## Notes

Do not use the **unescape** function to decode URIs. Use [decodeURI](/javascript/decodeURI) and [decodeURIComponent](/javascript/decodeURIComponent) functions instead.

This function is deprecated and not recommended for use in new projects. Use with caution.

## See also

### Related articles

#### Deprecated

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

-   [MutationEvent](/dom/MutationEvent)

-   [attrChange](/dom/MutationEvent/attrChange)

-   [attrName](/dom/MutationEvent/attrName)

-   [initMutationEvent](/dom/MutationEvent/initMutationEvent)

-   [newValue](/dom/MutationEvent/newValue)

-   [prevValue](/dom/MutationEvent/prevValue)

-   [relatedNode](/dom/MutationEvent/relatedNode)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [escape](/javascript/escape)

-   **unescape**

### Other articles

-   [decodeURI Function](/javascript/decodeURI)
-   [decodeURIComponent Function](/javascript/decodeURIComponent)
-   [escape Function](/javascript/escape)
-   [String Object](/javascript/String)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dz4x90hk(v=vs.94).aspx)

