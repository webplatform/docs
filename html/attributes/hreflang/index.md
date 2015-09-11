---
title: hreflang
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/hreflang

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
Internationalization topics related to the `hreflang` attribute:

-   [Indicating the language of a link destination](http://www.w3.org/International/techniques/authoring-html#linkdestination)

## <span>Examples</span>

In the [**a**](/html/elements/a) element in the following example, the **HREFLANG** attribute specifies the language code of the U.S. version of English.

``` html
<A HREF="http://example.microsoft.com/..." HREFLANG="en-US">anchor text</A>
```

## <span>Notes</span>

### <span>Remarks</span>

You must set the value of this property before you can retrieve it. Language codes identify natural languages that are spoken, written, or otherwise used for the communication of information among people, and are defined and explained in [Internet-Draft: BCP 47](http://www.rfc-editor.org/rfc/bcp/bcp47.txt). Computer languages are explicitly excluded from language codes.

**hreflang** was introduced in Microsoft Internet Explorer 6

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `a`
-   `link`
