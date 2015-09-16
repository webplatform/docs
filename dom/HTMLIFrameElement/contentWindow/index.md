---
title: 'contentWindow'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/contentWindowEX1.htm'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLIFrameElement
    href: /dom/HTMLIFrameElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLIFrameElement/contentWindow

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLIFrameElement](/dom/HTMLIFrameElement)[dom/HTMLIFrameElement](/dom/HTMLIFrameElement)

## Syntax

``` js
var result = element.contentWindow;
element.contentWindow = value;
```

## Examples

The following example shows how to use the **contentWindow** property to change the URL of window objects contained inside several **iframe** objects.

``` html
<html>
<head>
<SCRIPT>
function fnNavigate()
{
    for(i=0;i<document.all.length;i++)
    {
        if(document.all(i).tagName=="IFRAME")
        {
            document.all(i).contentWindow.location = "http://www.msn.com";
        }
    }
}
</SCRIPT>
</HEAD>
<BODY>
<BUTTON onclick="fnNavigate();">Navigate Frames</BUTTON>
<P/>
<IFRAME SRC="http://www.microsoft.com" STYLE="width:100%;height:150px;">
</IFRAME>
<P/>
<IFRAME SRC="http://www.microsoft.com" STYLE="width:100%;height:150px;">
</IFRAME>
<P/>
<IFRAME SRC="http://www.microsoft.com" STYLE="width:100%;height:150px;"/>
</IFRAME>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/contentWindowEX1.htm)

## Notes

### Remarks

This property is useful if you do not know the [**id**](/html/attributes/id) of the **frame** or **iframe** you are accessing through a collection.

### Syntax

## See also

### Related pages

-   `frame`
-   `iframe`
-   frameElement[frameElement](/dom/HTMLElement)
