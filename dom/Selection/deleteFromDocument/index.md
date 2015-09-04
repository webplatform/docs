---
title: deleteFromDocument
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Deletes the selected nodes from a document.'
uri: dom/Selection/deleteFromDocument

---
# deleteFromDocument

## Summary

Deletes the selected nodes from a document.

*Method of [dom/Selection](/dom/Selection)*

## Syntax

``` {.js}
var result = selObj.deleteFromDocument();
```

## Return Value

Returns an object of type Number.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

In the following example, select the text and elements in the shaded section. When the mouse button is released, the selected items are deleted. Refresh the page to try again.

``` {.html}
<!DOCTYPE html>
    <html>
    <head>
    <title>Delete From Document</title>
        <script type="text/javascript">
        function deleteSelectedContent() {
        if (window.getSelection){                       //check for a selection
            var selection = window.getSelection();      //get a selection object
            selection.deleteFromDocument();             //remove content
            }
        }
        function refresh()
        {
          window.location.reload( false );              //reload our page
        }
    </script>
    </head>
    <body>
    <div onmouseup="deleteSelectedContent ()" style="background-color:#c0c0c0;"  >
<h1>Now you see it</h1>
<p>Select some text or elements on this page. When you release the mouse button, it will be gone. </p>
<h2>H2 header</h2>
<p>Some more sample text to <strong>delete</strong>.</p>
</div>
 <input type="button" value="Refresh page" onclick="refresh()"   />
    </body>
</html>
</html>
```

### Syntax

window.getSelection().deleteFromDocument();

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.deleteFromDocument](https://developer.mozilla.org/en-US/docs/Web/API/Selection.deleteFromDocument) Article]

Portions of this content come from the Microsoft Developer Network: [[deleteFromDocument Method](http://msdn.microsoft.com/en-us/library/ie/ff975176(v=vs.85).aspx) Article]

