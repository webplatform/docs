---
title: isCollapsed
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.isCollapsed](https://developer.mozilla.org/en-US/docs/Web/API/Selection.isCollapsed) Article]'
  - 'Microsoft Developer Network: [[isCollapsed Property](http://msdn.microsoft.com/en-us/library/ie/ff974692(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Selection
    href: /dom/Selection
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/Selection
standardization_status: 'W3C Working Draft'
summary: 'Retrieves whether a selection is collapsed or empty.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Selection/isCollapsed

---
## <span>Summary</span>

Retrieves whether a selection is collapsed or empty.

Property of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = selObj.isCollapsed;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

false - The selection is not collapsed.

true - The selection is collapsed or empty.

## <span>Examples</span>

This example uses **isCollapsed** to see whether a selection is empty or not. If the selection is not empty, the selected text is displayed.

``` html
<!DOCTYPE html>

<html>
  <head>


    <!-- This example shows the character offset from anchor node of your selection. -->
    <title>isCollapsed Example</title>
    <script type="text/javascript">
      function testCollapsed () {
        if (window.getSelection) {
          var oSel = window.getSelection();
          var oDisplayBox = document.getElementById('displayBox');

          if (oSel.isCollapsed) {
            oDisplayBox.innerHTML = "<p>Nothing is selected!</p>";
          }
          else {
            oDisplayBox.innerHTML = "<p>The text of the selection:\n" + oSel.toString() + "</p>";
          }
        }
      }
    </script>
  </head>

  <body>
    <p>
      Click the button below to get the text content.
      Use the mouse to select some text within this field.
      Then, click the button again to see if the selection is collapsed.
    </p>
    <input type="button" value="Is it collapsed" onclick="testCollapsed()" />
    <div id="displayBox"></div>
  </body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

A collapsed selection has its start and end points set to the same value, which renders it empty. Even a collapsed selection may have a rangeCount greater than 0. selObj.getRangeAt(0) may return a range that is also collapsed.

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
