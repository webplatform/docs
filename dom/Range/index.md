---
title: Range
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range](https://developer.mozilla.org/en-US/docs/Web/API/range) Article]'
  - 'Microsoft Developer Network: [[Range](http://msdn.microsoft.com/en-us/library/ie/hh772133(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The Range interface represents a fragment of a document that can contain nodes and parts of text nodes in a given document.'
tags:
  - API
  - Objects
  - DOM
uri: dom/Range

---
## <span>Summary</span>

The Range interface represents a fragment of a document that can contain nodes and parts of text nodes in a given document.

## <span>Properties</span>

API Name
:   Summary

[collapsed](/dom/Range/collapsed)
:   The Range.collapsed read-only property returns a Boolean flag indicating whether the start and end points of the Range are at the same position. It returns true if the start and end boundary points of the Range are the same point in the DOM, false if not.

[commonAncestorContainer](/dom/Range/commonAncestorContainer)
:   Returns the deepest node in which two boundary points exist.

[endContainer](/dom/Range/endContainer)
:   Retrieves the end point node of the current range.

[endOffset](/dom/Range/endOffset)
:   Returns a number representing where in the Range.endContainer the Range ends.

[startContainer](/dom/Range/startContainer)
:   Retrieves the starting node of a current range

[startOffset](/dom/Range/startOffset)
:   Retrieves the offset of the starting boundary point relative to the startContainer in the current range.

## <span>Methods</span>

API Name
:   Summary

[cloneContents](/dom/Range/cloneContents)
:   Returns a document fragment containing the nodes of a range. If any nodes are partially selected, their start or end nodes are included.

[cloneRange](/dom/Range/cloneRange)
:   Returns a new range with boundary points that are equal to the original range.

[collapse](/dom/Range/collapse)
:   Collapses (or removes) a range by moving the insertion point to the beginning or end of the current range.

[compareBoundaryPoints](/dom/Range/compareBoundaryPoints)
:   The Range.compareBoundaryPoints() method compares the boundary points of the Range with another one.

[deleteContents](/dom/Range/deleteContents)
:   Removes all contents within a selected range.

[detach](/dom/Range/detach)
:   Removes or detaches a Range object and associated resources form a document.

[extractContents](/dom/Range/extractContents)
:   Removes the contents of a range from a document or document fragment and puts it a new document fragment.

[insertNode](/dom/Range/insertNode)
:   Inserts a Node into the start of a Range object.

[selectNode](/dom/Range/selectNode)
:   Selects a range node and all of its contents.

[selectNodeContents](/dom/Range/selectNodeContents)
:   Sets the Range to contain the contents of a Node.

[setEnd](/dom/Range/setEnd)
:   Sets the end point of the range.

[setEndAfter](/dom/Range/setEndAfter)
:   Sets the end of a range to a point after a specific node.

[setEndBefore](/dom/Range/setEndBefore)
:   Sets the end of the range to a point before a specific node.

[setStart](/dom/Range/setStart)
:   Sets the starting point of a range

[setStartAfter](/dom/Range/setStartAfter)
:   Sets the starting point of the range to a point after a specific node.

[setStartBefore](/dom/Range/setStartBefore)
:   Sets the start point of a range to a point before a specific node.

[surroundContents](/dom/Range/surroundContents)
:   Moves the contents of a Range to a new parent node, placing the new parent node at the start position of the Range.

[toString](/dom/Range/toString)
:   Returns the contents of a Range as a string. This string contains only the data characters, no markup.

## <span>Events</span>

*No events.*

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## <span>Related specifications</span>

[CSS Object Model - View Module](http://dev.w3.org/csswg/cssom-view/#extensions-to-the-range-interface)
:   Working Draft

[DOM Parsing and Serialization](http://domparsing.spec.whatwg.org/#extensions-to-the-range-interface)
:   Living Standard

[DOM](http://dom.spec.whatwg.org/#interface-range)
:   Living Standard
