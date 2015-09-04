---
title: anchorNode
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the element or node that contains the start of the selection.'
uri: dom/Selection/anchorNode

---
# anchorNode

## Summary

Returns the element or node that contains the start of the selection.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Selection](/dom/Selection)</span></span>

## Syntax

``` {.js}
var node = selObj.anchorNode;
selObj.anchorNode = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

## Examples

The following example shows the text that you select, and all the text contained in the anchorNode element.

``` {.html}
<!DOCTYPE html>
<html>
  <head>
<!-- this example shows the text you selected, and all the text within the anchor node-->
    <title>AnchorNode Example</title>
    <script type="text/javascript">
      function getAnchorNode() {
        if (window.getSelection) {                      //only work if supported
           var selection = window.getSelection ();      //get the selection object
           var anchorNodeProp = selection.anchorNode;   //get the node object
           alert ( "Selected text: \n" + selection.toString() + "\nText related to the node: \n" + anchorNodeProp.toString());
           }
      }
    </script>
  </head>
<body>
<div onmouseup="getAnchorNode()">                       <!-- call this function when the mouse button is released -->
      <p>
        Select some text with your mouse within this field.
        When the left button is released, a dialog pops up with the anchor node.
      </p>
      <p>
        This is some more text to try as well.
      </p>
    </div>
  </body>
</html>
```

## Notes

### Remarks

Returns null if not successful. This is not supported by Windows Internet Explorer 8 or earlier versions. AnchorNode returns the value of the [**startContainer**](/dom/Range/startContainer) attribute of the first **Range** object in the list. See [**focusNode**](/dom/Selection/focusNode) to find the node that contains the end of a selection.

A user may make a selection from left to right (in document order) or right to left (reverse of document order). The anchor is where the user began the selection. This can be visualized by holding the Shift key and pressing the arrow keys on your keyboard. The selection's anchor does not move, but the selection's focus, the other end of the selection, does move.

### Syntax

startNode=selObj.anchorNode;

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.anchorNode](https://developer.mozilla.org/en-US/docs/Web/API/Selection.anchorNode) Article]

Portions of this content come from the Microsoft Developer Network: [[anchorNode Property](http://msdn.microsoft.com/en-us/library/ie/ff974688(v=vs.85).aspx) Article]

