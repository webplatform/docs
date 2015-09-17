---
title: 'src (script)'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: 'src (script)'
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Summary
  - Needs_Examples
uri: 'html/attributes/src (script)'

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
## Notes

### Remarks

A **script** element can use the **SRC** attribute to refer to code stored in an external script library. If a **script** element refers to an external library and also contains code local to the block defined by the element, the code in the external library is executed before the local code. Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **SRC** attribute depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **SRC** returns an absolute URL. The value specified by the page author is returned when **SRC** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8. In Microsoft Internet Explorer 5 and later, the **SRC** attribute of the **script** element can refer to an XML data set if the [**LANGUAGE**](/html/attributes/language) attribute is set to **XML**. The **SRC** attribute was first available in Microsoft Internet Explorer 3.022. The **src** property is exposed through the object model as of Microsoft Internet Explorer 4.0.

### Syntax

## See also

### Related pages

-   `script`
