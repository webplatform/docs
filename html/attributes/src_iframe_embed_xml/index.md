---
title: 'src (iframe, embed, xml)'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: 'src (iframe, embed, xml)'
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Summary
uri: 'html/attributes/src (iframe, embed, xml)'

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

This example uses the **src** property to change the **src** attribute of an **iframe**.

``` html
function changeFrame(){
  alert (document.all.iframe1.src);
  document.all.iframe1.src="http://www.microsoft.com/";
  alert (document.all.iframe1.src);
}
```

## Notes

### Remarks

Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **SRC** attribute of the **frame** and **iframe** elements depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **SRC** returns an absolute URL. The value specified by the page author is returned when **SRC** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8.

### Syntax

## See also

### Related pages

-   `applet`
-   `embed`
-   `frame`
-   `iframe`
-   `xml`
