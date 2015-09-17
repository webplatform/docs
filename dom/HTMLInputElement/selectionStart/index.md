---
title: 'selectionStart'
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
  - API_Object_Properties
  - DOM
uri: dom/HTMLInputElement/selectionStart

---
Property of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## Syntax

``` js
var result = element.selectionStart;
element.selectionStart = value;
```

## Examples

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

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.2

## See also

### Related pages

-   `input type=text`
-   `textArea`
-   HTMLInputElement[HTMLInputElement](/dom/HTMLInputElement)
