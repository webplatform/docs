---
title: type (param element)
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - "\nMerge Candidate:  This page is a candidate for merge with the following pages: [[html/attributes/type]] \n\n"
uri: 'html/attributes/type (param element)'

---
# type (param element)

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Applies to
:    ?

## Examples

The following example shows how to use the **param** element to specify a run-time parameter for the object specified by the **object** element. A URI is specified for the Windows Media Player control.

    <OBJECT CLASSID="clsid:22D6F312-B0F6-11D0-94AB-0080C74C7E95">
    <PARAM NAME="FileName"
    VALUE="http://msdn.microsoft.com/workshop/samples/author/behaviors/media/28movie.asf"
    VALUETYPE="ref" TYPE="video/*"/>
    </OBJECT>

## Notes

### Remarks

The content type specifies the nature of a linked resource. Examples of content types include "text/html", "image/png", "image/gif", "video/mpeg", "audio/basic", "text/tcl", "text/javascript", and "text/vbscript". For the current list of registered content types, see [MIME Media Types](http://go.microsoft.com/fwlink/p/?linkid=203647). **type** was introduced in Microsoft Internet Explorer 6

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related pages (MSDN)

-   `param`
-   `Conceptual`
-   `Binding HTML Elements to Data`
-   `Introduction to Data Binding`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

