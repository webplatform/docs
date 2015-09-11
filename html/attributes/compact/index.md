---
title: compact
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/compact.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/compact

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## <span>Examples</span>

The following example shows how to use the **compact** property in HTML. Note that the presence of the word **COMPACT** sets the **compact** property to **true**

``` html
<HTML>
<BODY>
<DL COMPACT>
<DT>Cat
<DD>A small domesticated mammal.
<DT>Lizard
<DD>A reptile generally found in dry areas.
</DL>
</BODY>
</HTML>
```

The following example shows how to set the **compact** property using JScript

``` html
<HTML>
<BODY>
<script>
//Function that toggles the compact property for the DL element below
function compactDLToggle()
{
animals.compact = !animals.compact;
toggle.innerText = "Compact = "+animals.compact;
}
</script>
<P style="color:blue; font-weight:bold">Effect of setting COMPACT property for a DL element</P>
<BUTTON id="toggle" onclick="compactDLToggle()">Toggle Compact Property</BUTTON>
<DL id=animals>
<DT>Cat
<DD>A small domesticated mammal.
<DT>Lizard
<DD>A reptile generally found in dry areas.
</DL>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/compact.htm)

## <span>Notes</span>

### <span>Remarks</span>

There is no functionality implemented for the **compact** property for the **ul**, **ol**, **dir** and **menu** elements unless defined by the author. In Microsoft Internet Explorer 6 and greater, this property applies to the **menu** and **dir** objects.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 10.2 (Deprecated)

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `menu`
-   `dir`
-   `dl`
-   `ul`
-   `ol`
