---
title: 'collapse'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.collapse](https://developer.mozilla.org/en-US/docs/Web/API/Selection.collapse) Article]'
  - 'Microsoft Developer Network: [[collapse Method](http://msdn.microsoft.com/en-us/library/ie/ff975173(v=vs.85).aspx) Article]'
notes:
  - "The previous note said -\nMSDN documentation is incorrect.\noffset may have 0 or 1 value;\noffset\n\n   0 - Collapses the selection from the anchor to the beginning of parentNode's text.\n   1 - Collapses the selection from the anchor to the end of parentNode's text.\n\nHowever, testing in Chrome, values other than 0 or 1 are supported and are affecting the position of the caret accordingly."
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Selection
    href: /dom/Selection
standardization_status: 'W3C Working Draft'
summary: 'Replaces the current selection with an empty selection (or a caret) at the given offset.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Selection/collapse

---
## Summary

Replaces the current selection with an empty selection (or a caret) at the given offset.

Method of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

``` js
 selObj.collapse(/* see parameter list */);
```

## Parameters

### parentNode

 Data-type
:   DOM Node

 The parent node that the selection is contained in.

### offset

 Data-type
:   Number

**TODO**: Verify these values, as Chrome seems to respect values other than 0 or 1 and act accordingly.

       0 - Collapses the selection from the anchor to the beginning of parentNode's text.
       1 - Collapses the selection from the anchor to the end of parentNode's text.

## Return Value

No return value

## Examples

Place the caret at the beginning of an HTML document's body.

``` js
var body = document.getElementsByTagName('body')[0];
var selObj = window.getSelection();
selObj.collapse(body,0);// offset 0
```

## Notes

Throws a WrongDocumentError [**DOMException**](/dom/DOMException) if the *parentNode* is in another document. Throws a TypeError [**DOMException**](/dom/DOMException) if the relevantly typed arguments are not specified.

## Related specifications

[HTML Editing APIs](https://dvcs.w3.org/hg/editing/raw-file/tip/editing.html#dom-selection-collapse)
:   W3C Community Group Work In Progress

[HTML5 (Expired)](http://www.w3.org/TR/2010/WD-html5-20100624/editing.html#selection-0)
:   W3C Working Draft (Expired)
