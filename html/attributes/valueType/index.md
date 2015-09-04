---
title: valueType
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
uri: html/attributes/valueType

---
# valueType

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

**valueType** was introduced in Microsoft Internet Explorer 6

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

