---
title: isDisabled
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, compatibility, general discussion'
uri: dom/HTMLElement/isDisabled

---
# isDisabled

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.isDisabled;
element.isDisabled = value;
```

## Examples

The following example shows how to use the **isDisabled** property to determine whether an object is disabled.

    <HEAD>
    <SCRIPT>
    function chgInput() {
        currentState = oTextInput.isDisabled;
        newState = !currentState;
        oTextInput.disabled = newState;
        oCurrentValue.innerText = newState;
        newState==true ? oBtn.innerText="Enable" : oBtn.innerText="Disable"
    }
    </SCRIPT>
    </HEAD>
    <BODY onload="oCurrentValue.innerText = oTextInput.isDisabled;">
    <P>Click the button to enable or disable the <B>INPUT</B>.</P>
    <P>
    <INPUT ID="oBtn" TYPE="button" VALUE="Disable" onclick="chgInput()" />
    </P>
    <P><INPUT ID="oTextInput" VALUE="This is some text." /></P>
    Input disabled: <SPAN ID="oCurrentValue"></SPAN>
    </BODY>

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

