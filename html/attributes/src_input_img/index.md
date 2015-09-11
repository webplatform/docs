---
title: src (input, img)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/src.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: 'html/attributes/src (input, img)'

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
The required src attribute specifies the URL of the image.

Note: When a web page loads; it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stay in the same spot in relation to the web page, otherwise your visitors will get a broken link icon. The broken link icon is shown if the browser cannot find the image.

## <span>Examples</span>

This example uses the [**src**](/html/attributes/src_(iframe,_embed,_xml)) property to change the image's **src** attribute.

``` html
<body onmousedown="oImage.src='sphere.png'" onmouseup="oImage.src='cone.png'">
...
    <img id="oImage" src="cone.jpeg">

</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/src.htm)

## <span>Notes</span>

### <span>Remarks</span>

The value of the [**src**](/html/attributes/src_(iframe,_embed,_xml)) attribute of the **img** and **input type=image** elements depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **src** returns a URL relative to the hosting domain. The value specified by the page author is returned when **src** is read as a content attribute, when the page is displayed in an earlier document compatibility mode. Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the [**src**](/html/attributes/src_(iframe,_embed,_xml)) attribute of the **img** and **input type=image** elements depends on the context of the reference to the attribute. When read as a DOM attribute, **src** returns a URL relative to the domain hosting the Web page. The value specified by the page author is returned when **src** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `img`
-   `input type=image`
-   `HTMLInputElement`
