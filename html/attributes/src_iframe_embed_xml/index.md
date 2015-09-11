---
title: src (iframe, embed, xml)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: 'html/attributes/src (iframe, embed, xml)'

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

This example uses the **src** property to change the **src** attribute of an **iframe**.

``` html
function changeFrame(){
  alert (document.all.iframe1.src);
  document.all.iframe1.src="http://www.microsoft.com/";
  alert (document.all.iframe1.src);
}
```

## <span>Notes</span>

### <span>Remarks</span>

Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **SRC** attribute of the **frame** and **iframe** elements depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **SRC** returns an absolute URL. The value specified by the page author is returned when **SRC** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `applet`
-   `embed`
-   `frame`
-   `iframe`
-   `xml`
