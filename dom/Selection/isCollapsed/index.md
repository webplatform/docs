---
title: isCollapsed
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Retrieves whether a selection is collapsed or empty.'
uri: dom/Selection/isCollapsed

---
# isCollapsed

## Summary

Retrieves whether a selection is collapsed or empty.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Selection](/dom/Selection)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = selObj.isCollapsed;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

false - The selection is not collapsed.

true - The selection is collapsed or empty.

## Examples

This example uses **isCollapsed** to see whether a selection is empty or not. If the selection is not empty, the selected text is displayed.

``` {.html}
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

## Notes

### Remarks

A collapsed selection has its start and end points set to the same value, which renders it empty. Even a collapsed selection may have a rangeCount greater than 0. selObj.getRangeAt(0) may return a range that is also collapsed.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.isCollapsed](https://developer.mozilla.org/en-US/docs/Web/API/Selection.isCollapsed) Article]

Portions of this content come from the Microsoft Developer Network: [[isCollapsed Property](http://msdn.microsoft.com/en-us/library/ie/ff974692(v=vs.85).aspx) Article]

