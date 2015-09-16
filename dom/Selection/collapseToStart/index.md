---
title: collapseToStart
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Selection
    href: /dom/Selection
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Selection
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Selection/collapseToStart

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

``` js
var object = object.collapseToStart();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

The following code example puts the caret or insertion point at the beginning of the selected text.

``` html
<!DOCTYPE html>
<html>
<head>
   <title>Collapse to Start Example</title>
    <script>
        function SelectAtStart () {
            if (window.getSelection) {
                var selection = window.getSelection ();
                selection.collapseToStart ();
            }
        }
    </script>
</head>
<body>
<p>
    <div contenteditable="true" style="width:300px;">
        Select some text from this paragraph, and then click the following button.
        When you click the button, the caret, or insertion point, is set to the beginning of your selection.
    </div>
 </p>
 <p><input type="button" name="test" value="Set caret" onclick="SelectAtStart ()" /> </p>
</body>
</html>
```

## Notes

### Remarks

Raises an INVALID\_STATE [**DOMException**](/dom/DOMException) if there are no Ranges in the selection.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
