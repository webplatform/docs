---
title: select
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Not sure if this http://www.w3.org/TR/DOM-Level-2-HTML/html is a standard or not.... the MSDN doco has not w3 ref.... see Elliot/MSFT.'
summary: 'Makes the selection equal to the current object. '
uri: dom/TextRange/select

---
# select

## Summary

Makes the selection equal to the current object.

*Method of [dom/TextRange](/dom/TextRange)*

## Syntax

``` {.js}
var result = range.select();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

When applied to a TextRange object, the select method causes the current object to be highlighted. The following function uses the findText method to set the current object to the text in the TextRange object. The function assumes an element that contains the text string "text here".

``` {.js}
function TextRangeSelect() {
    var r = document.body.createTextRange();
    r.findText("text here");
    r.select();
}
```

When applied to a controlRange collection, the select method produces a shaded rectangle around the elements in the controlRange. The following function uses the add method to set the current object to an element in the controlRange collection. The function assumes an element with an id of "aaa".

``` {.js}
function ControlRangeSelect() {
    var r = document.body.createControlRange();
    r.add(document.all.aaa);
    r.select();
}
```

## Usage

     Used to programmatically select/highlight text and/or controls in a web document.

## Notes

### Remarks

This method causes the current object to be highlighted. When applied to a [**TextRange**](/dom/TextRange) object, the select method causes the current object to be highlighted. The following function uses the **findText** method to set the current object to the text in the **TextRange** object. The function assumes an element that contains the text string "text here".

    function TextRangeSelect() {
        var r = document.body.createTextRange();
        r.findText("text here");
        r.select();
    }

This method produces a shaded rectangle around the elements in the [**controlRange**](/dom/HTMLElement/controlRange). When applied to a **controlRange** collection, the select method produces a shaded rectangle around the elements in the **controlRange**. The following function uses the add method to set the current object to an element in the **controlRange** collection. The function assumes an element with an id of "aaa".

    function ControlRangeSelect() {
        var r = document.body.createControlRange();
        r.add(document.all.aaa);
        r.select();
    }

This feature might not be available on non-Microsoft Win32 platforms.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[select Method](http://msdn.microsoft.com/en-us/library/ie/ms536735(v=vs.85).aspx) Article]

