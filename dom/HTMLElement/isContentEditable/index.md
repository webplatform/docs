---
title: isContentEditable
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, compatibility, rearrange MSDN content to use WPD sections'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/editRegions.htm'
uri: dom/HTMLElement/isContentEditable

---
# isContentEditable

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.isContentEditable;
element.isContentEditable = value;
```

## Examples

The following example shows how to use the **isContentEditable** property to determine whether the user can edit the content of an object.

    <head>
    <SCRIPT>
    function chgSpan() {
        currentState = oSpan.isContentEditable;
        newState = !currentState;
        oSpan.contentEditable = newState;
        oCurrentValue.innerText = newState;
        newState==false ? oBtn.innerText="Enable Editing" :
            oBtn.innerText="Disable Editing"
    }
    </SCRIPT>
    </head>
    <body onload="oCurrentValue.innerText = oSpan.isContentEditable;">
    <P>Click the button to enable or disable SPAN content editing.</P>
    <P>
    <BUTTON ID="oBtn" onclick="chgSpan()">Enable Editing</BUTTON>
    </P>
    <P><SPAN ID="oSpan">You can edit this text.</SPAN></P>
    Span can be edited: <SPAN ID="oCurrentValue"></SPAN>
    </body>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/editRegions.htm)

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

