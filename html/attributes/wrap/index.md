---
title: wrap
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Sets the wrap style (soft, hard, or off) for a text element.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/wrap.htm'
uri: html/attributes/wrap

---
# wrap

## Summary

Sets the wrap style (soft, hard, or off) for a text element.

Applies to
:   dom/HTMLElement

## Examples

This example dynamically sets the **wrap** property of a **textArea** to the value selected by the user.

``` {.js}
<script>
function ChangeWrap(oSelect, oTA)
{
    cValue = oSelect.options(oSelect.selectedIndex).value;
    oTA.wrap = cValue;
}
</script>
...
<select id=cboWrap onchange="ChangeWrap(this, txt1)">
<option value=soft>soft
<option value=hard>hard
<option value=off>off
</select>
<p>
<textarea id=txt1 style="height:200;width:200"></textarea>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/wrap.htm)

## Notes

### Remarks

To detect the difference between **soft** and **hard** you must submit the content within the **textArea** to an HTTP server.

## Related specifications

Specification
:   Status
[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/)
:   W3C Working Draft

## See also

### Related pages (MSDN)

-   `textArea`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

