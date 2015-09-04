---
title: replaceWholeText
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: Deprecated
notes:
  - "Needs example....\nleave for me..."
summary: 'Replaces the text of the current object.'
uri: dom/Text/replaceWholeText

---
# replaceWholeText

## Summary

Replaces the text of the current object.

*Method of [dom/Text](/dom/Text)*

## Syntax

``` {.js}
var textNode = textNode.replaceWholeText(/* see parameter list */);
```

## Parameters

### text

 Data-typeÂ
:   String

 The text that replaces the existing text.

## Return Value

Returns an object of type DOM Node.

A [**Text**](/dom/Text) node that received the replacement text. If the replaced text was empty, this value will be null. If the current node is read-only, a new **Text** node is returned. If the current node is not read-only, the same object is returned.

**Needs Examples**: This section should include examples.

## Notes

Obsolete

This feature is obsolete. Although it may still work in some browsers, its use is discouraged since it could be removed at any time. Try to avoid using it.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
[DOM](http://dom.spec.whatwg.org/#text)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Text.replaceWholeText](https://developer.mozilla.org/en-US/docs/Web/API/Text.replaceWholeText) Article]

Portions of this content come from the Microsoft Developer Network: [[replaceWholeText Method](http://msdn.microsoft.com/en-us/library/ie/ff975208(v=vs.85).aspx) Article]

