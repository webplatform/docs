---
title: canHaveHTML
tags:
  - API
  - Object
  - Properties
  - DOM
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/canHaveHTML.htm'
uri: dom/HTMLElement/canHaveHTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected

---
# canHaveHTML

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.canHaveHTML;
element.canHaveHTML = value;
```

## Examples

The following example shows how to use the **canHaveHTML** property to determine whether an object can contain HTML markup.

    <HTML>
    <HEAD>
    <SCRIPT>
    function answer(arg) {
        arg ? alert("Yes") : alert("No");
    }
    </SCRIPT>
    </HEAD>
    <BODY>
    <P>INPUT: <INPUT type="text" ID="oInput" VALUE="oInput" /></P>
    <P>SPAN: <SPAN ID="oSpan">oSpan</SPAN></P>
    <BUTTON onclick="answer(oInput.canHaveHTML);">
    Can the INPUT contain HTML?
    </BUTTON>&nbsp;
    <BUTTON onclick="answer(oSpan.canHaveHTML);">
    Can the SPAN contain HTML?
    </BUTTON>
    </BODY>
    </HTML>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/canHaveHTML.htm)

## Notes

### Remarks

The property is read-only for all objects except the following, for which it is read-write: [**defaults**](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1).

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

