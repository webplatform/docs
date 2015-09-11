---
title: unescape
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dz4x90hk(v=vs.94).aspx)'
notes:
  - 'Deletion candidate; deprecated function'
readiness: 'Not Ready'
summary: "Deprecated\n"
tags:
  0: JS
  1: Basic
  3: Function
uri: javascript/unescape

---
## <span>Summary</span>

Deprecated

The deprecated **unescape()** function decodes a string that is usually encoded with the **escape** function.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    unescape(str)

**str**
:   Required. A String to be decoded

## <span>Examples</span>

``` js
unescape("webplatform"); // "webplatform"
unescape("%FCmlaut"); // "ümlaut"
unescape("%u65E5%u672C%u8A9E"); // "日本語"
```

## <span>Remarks</span>

All characters encoded with the % xx hexadecimal form are replaced by their ASCII character set equivalents.

Characters encoded in **%u** xxxx format (Unicode characters) are replaced with the Unicode character with hexadecimal encoding xxxx.

## <span>Notes</span>

Do not use the **unescape** function to decode URIs. Use [decodeURI](/javascript/decodeURI) and [decodeURIComponent](/javascript/decodeURIComponent) functions instead.

This function is deprecated and not recommended for use in new projects. Use with caution.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Deprecated</span>

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

### <span>Other articles</span>

-   [decodeURI Function](/javascript/decodeURI)
-   [decodeURIComponent Function](/javascript/decodeURIComponent)
-   [escape Function](/javascript/escape)
-   [String Object](/javascript/String)

