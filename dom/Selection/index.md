---
title: Selection
tags:
  - API
  - Objects
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'New listing page with proper object capitalization; replaces selection.'
summary: 'Represents the text selection in the greater page, possibly spanning multiple elements, when the user drags over static text and other parts of the page.'
uri: dom/Selection

---
# Selection

## Summary

Represents the text selection in the greater page, possibly spanning multiple elements, when the user drags over static text and other parts of the page.

## Overview

Selection is the class of the object returned by [window.getSelection()](/dom/Window/getSelection) and other methods. For information about text selection in an individual text editing element, see [Input](/dom/HTMLInputElement), [TextArea](/dom/HTMLTextAreaElement) and [document.activeElement](/dom/Document/activeElement) which typically return the parent object returned from window.getSelection().

## Properties

API Name
:   Summary
[anchorNode](/dom/Selection/anchorNode)
:   Returns the element or node that contains the start of the selection.
[anchorOffset](/dom/Selection/anchorOffset)
:   Returns the number of characters that the selection's anchor is offset within the anchorNode.
[focusNode](/dom/Selection/focusNode)
:   Retrieves the element or node that contains the end of a selection.
[focusOffset](/dom/Selection/focusOffset)
:   Returns the number of characters that the selection's focus is offset within the focusNode.
[isCollapsed](/dom/Selection/isCollapsed)
:   Retrieves whether a selection is collapsed or empty.
[rangeCount](/dom/Selection/rangeCount)
:   Returns the number of ranges in a selection
[typeDetail](/dom/Selection/typeDetail)
:

## Methods

API Name
:   Summary
[addRange](/dom/Selection/addRange)
:   Adds a Range to the current selection.
[clear](/dom/Selection/clear)
:   The clear() method is not in HTMLSelection Object.

    Use the removeAllRanges Method instead.

[collapse](/dom/Selection/collapse)
:   Replaces the current selection with an empty selection (or a caret) at the given offset.
[collapseToEnd](/dom/Selection/collapseToEnd)
:   Collapses or sets the insertion point or caret at the end of a selection object.

    If the content the selection is in is focused and editable, the caret will blink there.

[collapseToStart](/dom/Selection/collapseToStart)
:
[createRange](/dom/Selection/createRange)
:
[createRangeCollection](/dom/Selection/createRangeCollection)
:
[deleteFromDocument](/dom/Selection/deleteFromDocument)
:   Deletes the selected nodes from a document.
[getRangeAt](/dom/Selection/getRangeAt)
:   Returns a specified Range from a selection. The Range is specified by an index and cannot be greater than the number that is returned by rangeCount.
[removeAllRanges](/dom/Selection/removeAllRanges)
:   Removes all ranges from a selection.
[removeRange](/dom/Selection/removeRange)
:   Removes a range from a selection.
[selectAllChildren](/dom/Selection/selectAllChildren)
:   Adds all the children of the specified node to the selection. Previous selection is lost.

## Events

*No events.*

## Examples

A selection object represents the ranges that the user has selected. Typically, it holds only one range, accessed as follows:

``` {.js}
var selObj = window.getSelection();
if(selObj.rangeCount){ range  = selObj.getRangeAt(0);}
```

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection Object](https://developer.mozilla.org/en-US/docs/Web/API/Selection) Article]

Portions of this content come from the Microsoft Developer Network: [[HTMLSelection Object](http://msdn.microsoft.com/en-us/library/ie/ff974359(v=vs.85).aspx) Article]

