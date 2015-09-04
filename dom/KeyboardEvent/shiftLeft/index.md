---
title: shiftLeft
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
standardization_status: Non-Standard
notes:
  - 'Summary, examples, clean-up of MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm'
uri: dom/KeyboardEvent/shiftLeft

---
# shiftLeft

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/KeyboardEvent](/dom/KeyboardEvent)</span></span>

## Syntax

``` {.js}
var result = element.shiftLeft;
element.shiftLeft = value;
```

## Examples

The following example shows how to use the **shiftLeft** property to indicate when the user presses the left or right SHIFT keys.

    <HEAD>
    <SCRIPT>
    function init() {
        spanLeftShift.innerText='false';
        spanRightShift.innerText='false';
    }

    function indicate(obj, arg) {
        obj.innerText=arg;
    }

    function ShiftDown() {
        if (event.shiftLeft) {
            indicate(spanLeftShift,'true');
        }
        else {
            if (event.shiftKey) {
            indicate(spanRightShift,'true');
            }
        }
    }

    function ShiftUp() {
        if (!event.shiftKey) {
            indicate(spanLeftShift,'false');
            indicate(spanRightShift,'false');
        }
    }
    </SCRIPT>
    </HEAD>

    <BODY onload="document.body.focus(); init()" onkeydown="ShiftDown();" onkeyup="ShiftUp();">

    <P>Press either the left or right SHIFT key.</P>
    <TABLE>
    <TR>
    <TD><I>Left SHIFT Key Pressed</I></TD>
    <TD><I>Right SHIFT Key Pressed</I></TD>
    </TR>
    <TR>
    <TD ALIGN="center"><SPAN ID="spanLeftShift"></SPAN></TD>
    <TD ALIGN="center"><SPAN ID="spanRightShift"></SPAN></TD>
    </TR>
    </TABLE>
    </P>
    </BODY>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm)

## Notes

### Remarks

The [Document](/dom/Document) must have [**focus**](/dom/HTMLElement/focus) for this property to return true.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

