---
title: setSelectionRange
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'needs summary, clean-up MSDN import'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLInputElement
    href: /dom/HTMLInputElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLInputElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLInputElement/setSelectionRange

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## Syntax

``` js
var object = object.setSelectionRange(start, end);
```

## Parameters

### start

 Data-type
:   any

 The offset into the text field for the start of the selection.

### end

 Data-type
:   any

 The offset into the text field for the end of the selection.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

The following code example shows how to set a test selection's start and end positions.

``` html
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="X-UA-Compatible" content="IE=9" /> <!--Force IE9 mode -->
<title>Example of setSelectionRange()</title>
    <script>
        function SelectSomeText () {
            var input = document.getElementById ("Textbox");
                input.setSelectionRange (4,13);
        }
    </script>
</head>
<body>
    <p><input type="text" id="Textbox" size="40" value="The text selection appears here"/></p>
    <p><button onclick="SelectSomeText ()">See selection</button></p>

</body>
</html>
```

## Notes

### Remarks

If you set a parameter to more than the length of the text field, the parameter points to the end of the text field. If the *end* parameter is less than or equal to the *start* paramenter, the start and end positions of the selection are set to the *end* value. The selection is then an insertion point or caret.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.2

## See also

### Related pages (MSDN)

-   `input type=text`
-   `textArea`
