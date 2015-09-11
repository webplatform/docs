---
title: focusOffset
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.focusOffset](https://developer.mozilla.org/en-US/docs/Web/API/Selection.focusOffset) Article]'
  - 'Microsoft Developer Network: [[focusOffset Property](http://msdn.microsoft.com/en-us/library/ie/ff974691(v=vs.85).aspx) Article]'
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
summary: 'Returns the number of characters that the selection''s focus is offset within the focusNode.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Selection/focusOffset

---
## <span>Summary</span>

Returns the number of characters that the selection's focus is offset within the focusNode.

Property of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var offset = selObj.focusOffset;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

The following example uses **focusOffset** to show the offset value for the end of a selection when you release the mouse button.

``` html
<!DOCTYPE html>
<html>
  <head>
<!-- this example displays the character offset from anchor node of your selection-->
    <title>Focus Offset Example</title>
    <script type="text/javascript">
      function getfocusOffset() {
        if (window.getSelection) {                      //only works if supported
           var selection = window.getSelection ();      //get the selection object
           var focusOffsetProp = selection.focusOffset;   //get the offset
           alert ( "Offset: \n" + focusOffsetProp.toString());
           }
      }
    </script>
  </head>
<body>
<div onmouseup="getfocusOffset()">    <!-- call the function when the mouse button is released -->
      <p>
        Use the mouse to select some text within this field.
        When <strong>the left <em>button</em> is released</strong>, a dialog box appears with the anchor offset.
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

**focusOffset** typically refers to a character position within the text portion of the [**focusNode**](/dom/Selection/focusNode).

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
