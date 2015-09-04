---
title: isMultiLine
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, compatibility, rearrange MSDN content to use WPD sections'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ismultilineEX1.htm'
uri: dom/HTMLElement/isMultiLine

---
# isMultiLine

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.isMultiLine;
element.isMultiLine = value;
```

## Examples

The following example shows how to use the **isMultiLine** property to determine whether the content of an object can contain only one line or multiple lines of text.

    <HTML>
    <HEAD>
    <SCRIPT>
    function answer(arg) {
        arg ? alert("Yes") : alert("No");
    }
    </SCRIPT>
    </HEAD>
    <BODY>
    <P>INPUT: <INPUT type="text" ID="oInput" VALUE="oInput"/>
    <BUTTON onclick="answer(oInput.isMultiLine);">
    Can the INPUT contain more than one line?</BUTTON>
    </P>

    <P>TEXTAREA: <TEXTAREA ID="oTextarea">oTextarea</TEXTAREA>
    <BUTTON onclick="answer(oTextarea.isMultiLine);">
    Can the TEXTAREA contain more than one line?</BUTTON>
    </P>
    </BODY>
    </HTML>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ismultilineEX1.htm)

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

