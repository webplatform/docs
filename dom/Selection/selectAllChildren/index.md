---
title: selectAllChildren
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.selectAllChildren](https://developer.mozilla.org/en-US/docs/Web/API/Selection.selectAllChildren) Article]'
  - 'Microsoft Developer Network: [[selectAllChildren Method](http://msdn.microsoft.com/en-us/library/ie/ff975180(v=vs.85).aspx) Article]'
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
summary: 'Adds all the children of the specified node to the selection. Previous selection is lost.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Selection/selectAllChildren

---
## Summary

Adds all the children of the specified node to the selection. Previous selection is lost.

Method of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

``` js
var result = selObj.selectAllChildren(/* see parameter list */);
```

## Parameters

### parentNode

 Data-type
:   DOM Node

 The object that receives the new selection.

## Return Value

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

In this example, your selection is replaced by all the elements of the DIV.

``` html
<!DOCTYPE html>
<head>
    <title>Select all children example</title>
    <script>
        function selectAllChildrenDemo () {
            var getNode = document.getElementById ("elementID");
            if (window.getSelection) {        // Internet Explorer 9
                var selection = window.getSelection ();
                selection.selectAllChildren (getNode);
            } else {                          // Workaround for Internet Explorer 8 & earlier
                var oRange = document.body.createTextRange ();
                oRange.moveToElementText (getNode);
                oRange.select ();
            }
        }
    </script>
</head>
<body>
    <button onclick="selectAllChildrenDemo ();">Select everything below</button>
    <div id="elementID">The <strong>selectAllChildren</strong> method replaces the current <em>selection</em> with the all the <strong>contents</strong> of the specified element (in this case a DIV).</div>
</body>
```

``` js
var footer = document.getElementById("footer");
window.getSelection().selectAllChildren(footer);
/* Everything inside the footer is now selected */
```

## Notes

### Remarks

Raises a WRONG\_DOCUMENT\_ERR [**DOMException**](/dom/DOMException) if the *parentNode* is in another document.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
