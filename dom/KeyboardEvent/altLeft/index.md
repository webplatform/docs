---
title: altLeft
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Summary, examples, compatibility, standards, clean-up of MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm'
uri: dom/KeyboardEvent/altLeft

---
# altLeft

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/KeyboardEvent](/dom/KeyboardEvent)</span></span>

## Syntax

``` {.js}
var result = element.altLeft;
element.altLeft = value;
```

## Examples

The following example shows how to use the **altLeft** property to indicate when the user presses the left or right ALT keys.

    <HEAD>
    <SCRIPT>
    function init() {
        spanLeftAlt.innerText='false';
        spanRightAlt.innerText='false';
    }

    function indicate(obj, arg) {
        obj.innerText=arg;
    }

    function AltDown() {
        if (event.altLeft) {
            indicate(spanLeftAlt,'true');
        }
        else {
            if (event.altKey) {
                 indicate(spanRightAlt,'true');
            }
        }
    }

    function AltUp() {
        if (!event.altKey) {
            indicate(spanLeftAlt,'false');
            indicate(spanRightAlt,'false');
        }
    }
    </SCRIPT>
    </HEAD>

    <BODY onload="document.body.focus(); init()" onkeydown="AltDown();" onkeyup="AltUp();">

    <P>Press either the left or right ALT key.</P>
    <TABLE>
    <TR>
    <TD><I>Left ALT Key Pressed</I></TD>
    <TD><I>Right ALT Key Pressed</I></TD>
    </TR>
    <TR>
    <TD ALIGN="center"><SPAN ID="spanLeftAlt"></SPAN></TD>
    <TD ALIGN="center"><SPAN ID="spanRightAlt"></SPAN></TD>
    </TR>
    </TABLE>
    </P>
    </BODY>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm)

## Notes

### Remarks

This property is currently supported only in Microsoft Windows NT 4.0 and Windows 2000. The [Document](/dom/Document) must have **focus** for this property to return true. No **altRight** property is available. Authors can test for the right ALT key by using the **altKey** and **altLeft** properties.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

