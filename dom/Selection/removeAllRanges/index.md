---
title: removeAllRanges
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Selection.removeAllRanges](https://developer.mozilla.org/en-US/docs/Web/API/Selection.removeAllRanges) Article]'
  - 'Microsoft Developer Network: [[removeAllRanges Method](http://msdn.microsoft.com/en-us/library/ie/ff975178(v=vs.85).aspx) Article]'
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
summary: 'Removes all ranges from a selection.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Selection/removeAllRanges

---
## <span>Summary</span>

Removes all ranges from a selection.

Method of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## <span>Syntax</span>

``` js
var result = selObj.removeAllRanges();
```

## <span>Return Value</span>

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

This example uses **removeAllRanges** to clear a selection from text or elements.

``` html
<!DOCTYPE html>
<html>
    <head>
    <title>Remove All Ranges Example</title>
        <script type="text/javascript">
        function removeAllRangesDemo() {
        if (window.getSelection){                       //check for a selection
            var selection = window.getSelection();      //get a selection object
            selection.removeAllRanges();                //remove all ranges
            }
        }
    </script>
    </head>
    <body>
<h1>Remove all ranges example</h1>
<p>Select some text or elements on this page. When you click the button below, the selection will be cleared. </p>
<h2>H2 header</h2>
<p>Some more sample text to <strong>delete</strong>.</p>
<input type="button" value="Remove all Ranges" onclick="removeAllRangesDemo()"   />
    </body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

**removeAllRanges** can remove invisible carets or insertion points that result when the **Collapse** method is applied to a selection.

### <span>Syntax</span>

selObj.removeAllRanges();

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.1
