---
title: src (iframe, embed, xml)
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
uri: 'html/attributes/src (iframe, embed, xml)'

---
# src (iframe, embed, xml)

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Applies to
:    ?

## Examples

This example uses the **src** property to change the **src** attribute of an **iframe**.

    function changeFrame(){
      alert (document.all.iframe1.src);
      document.all.iframe1.src="http://www.microsoft.com/";
      alert (document.all.iframe1.src);
    }

## Notes

### Remarks

Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **SRC** attribute of the **frame** and **iframe** elements depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **SRC** returns an absolute URL. The value specified by the page author is returned when **SRC** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8.

### Syntax

## See also

### Related pages (MSDN)

-   `applet`
-   `embed`
-   `frame`
-   `iframe`
-   `xml`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

