---
title: selectionEnd
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLInputElement/selectionEnd

---
# selectionEnd

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLInputElement](/dom/HTMLInputElement)</span></span>

## Syntax

``` {.js}
var result = element.selectionEnd;
element.selectionEnd = value;
```

## Examples

The following code example shows how to set a text selection's start and end positions.

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

## Notes

### Remarks

If you do not select text, **selectionEnd** returns the offset of the character that immediately follows the text cursor or caret.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 7.6.2

## See also

### Related pages (MSDN)

-   `input type=text`
-   `textArea`
-   `HTMLInputElement`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

