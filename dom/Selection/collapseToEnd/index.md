---
title: collapseToEnd
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.collapseToEnd](https://developer.mozilla.org/en-US/docs/Web/API/Selection.collapseToEnd) Article]'
  - 'Microsoft Developer Network: [[collapseToEnd Method](http://msdn.microsoft.com/en-us/library/ie/ff975174(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Selection
    href: /dom/Selection
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Selection
standardization_status: 'W3C Working Draft'
summary: "Collapses or sets the insertion point or caret at the end of a selection object.\n"
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Selection/collapseToEnd

---
## Summary

Collapses or sets the insertion point or caret at the end of a selection object.

If the content the selection is in is focused and editable, the caret will blink there.

Method of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

``` js
var result = selObj.collapseToEnd();
```

## Return Value

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

The following code example puts the caret or insertion point at the end of the selected text.

``` html
<!DOCTYPE html>
<html>
<head>
   <title>Collapse to Start Example</title>
    <script>
        function SelectAtEnd () {
            if (window.getSelection) {
                var selection = window.getSelection ();
                selection.collapseToEnd ();
            }
        }
    </script>
</head>
<body>
<p>
    <div contenteditable="true" style="width:300px;">
        Select some text from this paragraph, and then click the following button.
        When you click the button, the caret, or insertion point, is set to the end of your selection.
    </div>
 </p>
 <p><input type="button" name="test" value="Set caret" onclick="SelectAtEnd ()" /> </p>
</body>
</html>
```

## Notes

### Remarks

Raises an INVALID\_STATE [**DOMException**](/dom/DOMException) if there are no Ranges in the selection.

### Syntax

selObj.collapseToEnd()

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
