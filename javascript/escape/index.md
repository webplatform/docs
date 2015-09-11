---
title: escape
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9yzah1fh(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: "Deprecated\n"
tags:
  - JS
  - Basic
uri: javascript/escape

---
## <span>Summary</span>

Deprecated

The deprecated **escape()** function encodes a string so it can be read on all computers.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    escape(str)

**str**
:   Required. A String to be encoded

## <span>Return Value</span>

Returns a string value in Unicode format that contains the encoded contents of the str parameter.

## <span>Examples</span>

``` js
unescape("webplatform"); // "webplatform"
unescape("ümlaut"); // "%FCmlaut"
unescape("日本語"); // "%u65E5%u672C%u8A9E"
```

## <span>Remarks</span>

All spaces, punctuation, accented characters, and any other non-ASCII characters are replaced with % xx encoding, where xx is equivalent to the hexadecimal number representing the character. For example, a space is returned as "%20."

Characters with a value greater than 255 are stored using the **%u** xxxx format.

## <span>Notes</span>

The **escape** function should not be used to encode URIs. Use [encodeURI](/javascript/encodeURI) and [encodeURIComponent](/javascript/encodeURIComponent) functions instead

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

-   **escape**

-   [unescape](/javascript/unescape)

### <span>Other articles</span>

-   [encodeURI Function](/javascript/encodeURI)
-   [encodeURIComponent Function](/javascript/encodeURIComponent)
-   [String Object](/javascript/String)
-   [unescape Function](/javascript/unescape)

