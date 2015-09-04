---
title: ctrlLeft
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Summary, compatibility, standards, clean-up of MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm'
uri: dom/KeyboardEvent/ctrlLeft
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/focus

---
# ctrlLeft

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/KeyboardEvent](/dom/KeyboardEvent)</span></span>

## Syntax

``` {.js}
var result = element.ctrlLeft;
element.ctrlLeft = value;
```

## Examples

The following example shows how to use the **ctrlLeft** property to indicate when the user presses the left or right CTRL keys.

    <HEAD>
    <SCRIPT>
    function init() {
        spanLeftCtrl.innerText='false';
        spanRightCtrl.innerText='false';
    }

    function indicate(obj, arg) {
        obj.innerText=arg;
    }

    function CtrlDown() {
        if (event.ctrlLeft) {
            indicate(spanLeftCtrl,'true');
        }
        else {
            if (event.ctrlKey) {
                indicate(spanRightCtrl,'true');
            }
        }
    }

    function CtrlUp() {
        if (!event.ctrlKey) {
            indicate(spanLeftCtrl,'false');
            indicate(spanRightCtrl,'false');
        }
    }
    </SCRIPT>
    </HEAD>

    <BODY onload="document.body.focus(); init()" onkeydown="CtrlDown();" onkeyup="CtrlUp();">

    <P>Press either the left or right CTRL key.</P>
    <TABLE>
    <TR>
    <TD><I>Left CTRL Key Pressed</I></TD>
    <TD><I>Right CTRL Key Pressed</I></TD>
    </TR>
    <TR>
    <TD ALIGN="center"><SPAN ID="spanLeftCtrl"></SPAN></TD>
    <TD ALIGN="center"><SPAN ID="spanRightCtrl"></SPAN></TD>
    </TR>
    </TABLE>
    </P>
    </BODY>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm)

## Notes

### Remarks

This property is currently supported only in Microsoft Windows NT 4.0 and Windows 2000. The [Document](/dom/Document) must have [**focus**](/w/index.php?title=dom/methods/focus&action=edit&redlink=1) for this property to return true.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

