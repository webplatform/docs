---
title: 'focusNode'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.focusNode](https://developer.mozilla.org/en-US/docs/Web/API/Selection.focusNode) Article]'
  - 'Microsoft Developer Network: [[focusNode Property](http://msdn.microsoft.com/en-us/library/ie/ff974690(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Selection
    href: /dom/Selection
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Selection
standardization_status: 'W3C Working Draft'
summary: 'Retrieves the element or node that contains the end of a selection.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Selection/focusNode

---
## Summary

Retrieves the element or node that contains the end of a selection.

Property of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

**Note**: This property is read-only.

``` js
var oNode = selObj.focusNode;
```

## Return Value

Returns an object of type DOM NodeDOM Node

Returns the node in which the selection ends.

## Examples

The following example shows the text content that is contained within the node (or tags) that is in focus when you click a section of text.

``` html
<!DOCTYPE html>
<html>
  <head>
<!-- this example displays the character offset from anchor node of your selection-->
    <title>focusNode Example</title>
    <script type="text/javascript">
      function getfocusNode() {
        if (window.getSelection) {                      //only work if supported
           var selection = window.getSelection ();      //get the selection object
           var focusNodeProp = selection.focusNode;     //get the node containing the end of selection
           alert ( "Text of current node: \n" + focusNodeProp.toString() + "\nTag name: <" + focusNodeProp.parentNode.tagName +">");
           }
      }
    </script>
  </head>
<body>
<div onmouseup="getfocusNode()">    <!-- call the function when the mouse button is released -->
      <p>
        Select some text with your mouse within this field.
        When <strong>the left <em>button</em> is released</strong>, a dialog box appears with the focusNode.
      </p>
      <p>
        The nested tags <strong>here and <em>there</em> can</strong> demonstrate different focusNodes as well.
      </p>
    </div>
  </body>
</html>
```

## Notes

### Remarks

Returns null if the selection does not exist. As a [**Selection**](/dom/Selection) object consists of a list of Range objects, focusNode returns the value of the [**endContainer**](/dom/Range/endContainer) attribute of the last Range object in the list.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
