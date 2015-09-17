---
title: 'escape'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9yzah1fh(v=vs.94).aspx)'
compatibility:
  feature: escape
  topic: javascript
readiness: 'Ready to Use'
summary: "Deprecated\n"
tags:
  - JS_Basic
uri: javascript/escape

---
## Summary

Deprecated

The deprecated **escape()** function encodes a string so it can be read on all computers.

## Syntax

    escape(str)

**str**
:   Required. A String to be encoded

## Return Value

Returns a string value in Unicode format that contains the encoded contents of the str parameter.

## Examples

``` js
unescape("webplatform"); // "webplatform"
unescape("ümlaut"); // "%FCmlaut"
unescape("日本語"); // "%u65E5%u672C%u8A9E"
```

## Remarks

All spaces, punctuation, accented characters, and any other non-ASCII characters are replaced with % xx encoding, where xx is equivalent to the hexadecimal number representing the character. For example, a space is returned as "%20."

Characters with a value greater than 255 are stored using the **%u** xxxx format.

## Notes

The **escape** function should not be used to encode URIs. Use [encodeURI](/javascript/encodeURI) and [encodeURIComponent](/javascript/encodeURIComponent) functions instead

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

-   **escape**

-   [unescape](/javascript/unescape)

### Other articles

-   [encodeURI Function](/javascript/encodeURI)
-   [encodeURIComponent Function](/javascript/encodeURIComponent)
-   [String Object](/javascript/String)
-   [unescape Function](/javascript/unescape)

