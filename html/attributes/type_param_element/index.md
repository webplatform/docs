---
title: type (param element)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "\nMerge Candidate:  This page is a candidate for merge with the following pages: [[html/attributes/type]] \n\n"
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: 'html/attributes/type (param element)'

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

The following example shows how to use the **param** element to specify a run-time parameter for the object specified by the **object** element. A URI is specified for the Windows Media Player control.

``` html
<OBJECT CLASSID="clsid:22D6F312-B0F6-11D0-94AB-0080C74C7E95">
<PARAM NAME="FileName"
VALUE="http://msdn.microsoft.com/workshop/samples/author/behaviors/media/28movie.asf"
VALUETYPE="ref" TYPE="video/*"/>
</OBJECT>
```

## <span>Notes</span>

### <span>Remarks</span>

The content type specifies the nature of a linked resource. Examples of content types include "text/html", "image/png", "image/gif", "video/mpeg", "audio/basic", "text/tcl", "text/javascript", and "text/vbscript". For the current list of registered content types, see [MIME Media Types](http://go.microsoft.com/fwlink/p/?linkid=203647). **type** was introduced in Microsoft Internet Explorer 6

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `param`
-   `Conceptual`
-   `Binding HTML Elements to Data`
-   `Introduction to Data Binding`
