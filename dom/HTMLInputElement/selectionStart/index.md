---
title: selectionStart
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLInputElement
    href: /dom/HTMLInputElement
standardization_status: Unknown
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLInputElement/selectionStart

---
Property of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## <span>Syntax</span>

``` js
var result = element.selectionStart;
element.selectionStart = value;
```

## <span>Examples</span>

The following code example shows how to set a text selection's start and end positions.

``` html
<!DOCTYPE html>
<html>
<head>
<title>Selection Start and End example</title>
    <script>
        function SelectSomeText () {
            var input = document.getElementById ("Textbox");
                input.selectionStart = 4;
                input.selectionEnd = 13;
        }
    </script>
</head>
<body>
    <p><input type="text" id="Textbox" size="40" value="The text selection appears here"/></p>
    <p><button onclick="SelectSomeText ()">See selection</button></p>

</body>
</html>
```

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.2

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `input type=text`
-   `textArea`
-   `HTMLInputElement`
