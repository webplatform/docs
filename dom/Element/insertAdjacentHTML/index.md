---
title: insertAdjacentHTML
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: Mixed
notes:
  - 'Needs compat'
summary: 'Parses and inserts HTML code at or beyond the edges of an element within the document hierarchy.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertscript_1.htm'
uri: dom/Element/insertAdjacentHTML

---
# insertAdjacentHTML

## Summary

Parses and inserts HTML code at or beyond the edges of an element within the document hierarchy.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
 element.insertAdjacentHTML(where, html);
```

## Parameters

### where

 Data-typeÂ
:   String

 Where to insert the HTML text. Must be one of the following values:

Value
:   Description
"beforebegin"
:   Before the element itself.
"afterbegin"
:   Just inside the element, before its first child.
"beforeend"
:   Just inside the element, after its last child.
"afterend"
:   After the element itself.

### html

 Data-typeÂ
:   String

 Well-formed HTML code to insert. The string can be a combination of text and HTML tags.

## Return Value

No return value

## Examples

This example uses the **insertAdjacentHTML** method to insert script into the page.

``` {.js}
var sHTML="<input type=button onclick=" +
    "go2()" + " value='Click Me'><BR>"
var sScript='<SCRIPT DEFER>'
sScript = sScript +
    'function go2(){ alert("Hello from inserted script.") }'
sScript = sScript + '</script' + '>';
ScriptDiv.insertAdjacentHTML("afterBegin",sHTML + sScript);
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertscript_1.htm)

## Usage

     Use this method to add HTML to the page before/after an element or at the beginning or at the end of an element.

## Notes

-   In XML documents, this methods will fail if the **html** parameter is not well-formed, valid HTML.
-   This method will fail if "afterend" or "beforebegin" is used when the context is the root element of the document.
-   If the text contains HTML tags, the method parses and formats the text as it is inserted.

**TODO**: The notes below need to be verified.

-   You cannot insert text while the document is loading. Wait for the [**onload**](/dom/Element/load) event to fire before attempting to call this method.
-   When using the **insertAdjacentHTML** method to insert script, you must include the [**DEFER**](/html/attributes/defer) attribute in the [**script**](/html/elements/script) element.

## Related specifications

Specification
:   Status
[DOM Parsing and Serialization](http://domparsing.spec.whatwg.org/)
:   Living Standard

## See also

### Related pages (MSDN)

-   `innerHTML`
-   `outerHTML`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

