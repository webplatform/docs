---
title: face
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/face.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves the current typeface family.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/face

---
## Summary

Sets or retrieves the current typeface family.

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
## Examples

This example sets the typeface family using the **FACE** attribute and the **face** property.

``` html
<FONT FACE="Arial" ID=oFont>
:
<SCRIPT>
    alert(oFont.face + "\n" + "When you click this, the font will change");
    oFont.face = 'Courier';
    alert(oFont.face + "\n" + "The font has changed.");
</SCRIPT>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/face.htm)

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 15.2.2 (Deprecated)

## See also

### Related pages (MSDN)

-   `baseFont`
-   `font`
-   `fontFamily`
