---
title: anchorOffset
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.anchorOffset](https://developer.mozilla.org/en-US/docs/Web/API/Selection.anchorOffset) Article]'
  - 'Microsoft Developer Network: [[anchorOffset Property](http://msdn.microsoft.com/en-us/library/ie/ff974689(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Selection
    href: /dom/Selection
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/Selection
standardization_status: 'W3C Working Draft'
summary: 'Returns the number of characters that the selection''s anchor is offset within the anchorNode.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Selection/anchorOffset

---
## <span>Summary</span>

Returns the number of characters that the selection's anchor is offset within the anchorNode.

Property of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var offset = selObj.anchorOffset;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

The following example shows the anchorOffset value of a selection when you release the mouse button.

``` html
<!DOCTYPE html>
<html>
  <head>
<!-- this example shows the character offset from anchor node of your selection-->
    <title>AnchorOffset Example</title>
    <script type="text/javascript">
      function getAnchorOffset() {
        if (window.getSelection) {                      //only work if supported
           var selection = window.getSelection ();      //get the selection object
           var anchorOffsetProp = selection.anchorOffset;   //get the offset
           alert ( "Anchor Offset: \n" + anchorOffsetProp.toString());
           }
      }
    </script>
  </head>
<body>
<div onmouseup="getAnchorOffset()">    <!-- call this function when the mouse button is released -->
      <p>
        Select some text with your mouse within this field.
        When <strong>the left <em>button</em> is released</strong>, a dialog pops up with the anchor offset.
      </p>
      <p>
        The nested tags <strong>here and <em>there</em> can</strong> demonstrate different offsets as well.
      </p>
    </div>
  </body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

The value that is returned by **anchorOffset** usually refers to a character position within the text portion of the element.

### <span>Syntax</span>

offset=selObj.anchorOffset;

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
