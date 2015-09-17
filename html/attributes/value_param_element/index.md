---
title: 'value (param element)'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: 'value (param element)'
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Summary
uri: 'html/attributes/value (param element)'

---
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

The following example shows how to use the **param** element to specify a run-time parameter for the object specified by the **object** element. A URI is specified for the Windows Media Player control.

``` html
<OBJECT CLASSID="clsid:22D6F312-B0F6-11D0-94AB-0080C74C7E95">
<PARAM NAME="FileName"
VALUE="http://msdn.microsoft.com/workshop/samples/author/behaviors/media/28movie.asf"
VALUETYPE="ref" TYPE="video/*"/>
</OBJECT>
```

## Notes

### Remarks

In Microsoft Internet Explorer 3.02 and later, **value** is an attribute of **param**. Beginning in Microsoft Internet Explorer 6, **value** is a read/write property.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related pages

-   `param`
-   `Conceptual`
-   `Binding HTML Elements to Data`
-   `Introduction to Data Binding`
