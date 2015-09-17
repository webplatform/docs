---
title: 'parentTextEdit'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec, and compat'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/Element/parentTextEdit

---
Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.parentTextEdit;
element.parentTextEdit = value;
```

## Examples

This example retrieves the parent object, if needed, creates the text range, moves to the original object, and selects the first word in the object.

``` html
<SCRIPT LANGUAGE="JScript">
function selectWord()
{
    var oSource = window.event.srcElement ;
    if (!oSource.isTextEdit)
        oSource = oSource.parentTextEdit;
    if (oSource != null) {
        var oTextRange = oSource.createTextRange();
        oTextRange.moveToElementText(window.event.srcElement);
        oTextRange.collapse();
        oTextRange.expand("word");
        oTextRange.select();
    }
}
</SCRIPT>
```

## Notes

### Remarks

The property is an object if the parent exists; otherwise, it is `null`. For example, the **parentTextEdit** property of the **body** is `null`.

### Syntax
