---
title: parentTextEdit
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec, and compat'
uri: dom/Element/parentTextEdit

---
# parentTextEdit

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

``` {.js}
var result = element.parentTextEdit;
element.parentTextEdit = value;
```

## Examples

This example retrieves the parent object, if needed, creates the text range, moves to the original object, and selects the first word in the object.

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

## Notes

### Remarks

The property is an object if the parent exists; otherwise, it is `null`. For example, the **parentTextEdit** property of the **body** is `null`.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

