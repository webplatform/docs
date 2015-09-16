---
title: accept
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Address minor bugs; Could be part of security considerations articles; General cleanup of links; Need to cross-link to other relevant content'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'This attribute supplies browsers with a hint about what filetypes its element will accept.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/accept

---
## Summary

This attribute supplies browsers with a hint about what filetypes its element will accept.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[HTMLInputElement](/dom/HTMLInputElement)

</td>
</tr>
</table>
Accepts a comma separated list of file types. Valid file types can be any of the following.

-   The string `audio/*` indicates any audio file is allowed.
-   The string `video/*` indicates any video file is allowed.
-   The string `image/*` indicates any image file is allowed.
-   A valid [[type](http://docs.webplatform.org/wiki/concepts/internet_and_web/mime_types%7Cmime)] with no attributes.
-   A file extension starting with a `.` (period).

Duplicates are not allowed (case insensitive).

## Examples

Indicates that audio files are accepted.

``` html
<input type="file" accept="audio/*" />
```

Indicates that both PNG and GIF file formats are accepted.

``` html
<input type="file" accept="image/png, image/gif" />
```

## Notes

### Remarks

The information from the list can be used to filter out nonconforming files when prompting a user to select files to be sent to the server using the **\<INPUT\> element with type="file"**. Examples of content types include "text/html", "image/png", "image/gif", "video/mpeg", "audio/basic", "text/tcl", "text/javascript", and "text/vbscript". For the current list of registered MIME types, see [MIME Media Types](http://go.microsoft.com/fwlink/p/?linkid=203647). There is no functionality implemented for this property unless defined by the author. **accept** was introduced in Microsoft Internet Explorer 6

## Related specifications

[HTML5](http://www.w3.org/TR/html5/forms.html#attr-input-accept)
:   W3C Candidate Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   **accept**

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   [checked](/html/attributes/checked)

-   [crossorigin](/html/attributes/crossorigin)

-   [form](/html/attributes/form)

-   [formEnctype](/html/attributes/formEnctype)

-   [height](/html/attributes/height)

-   [list](/html/attributes/list)

-   [max (HTMLInputElement)](/html/attributes/max_(HTMLInputElement))

-   [maxLength](/html/attributes/maxLength)

-   [min](/html/attributes/min)

-   [multiple](/html/attributes/multiple)

-   [readonly](/html/attributes/readonly)

-   [size](/html/attributes/size)

-   [standby](/html/attributes/standby)

-   [step](/html/attributes/step)

-   [HTML Elements](/html/elements)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [datalist](/html/elements/datalist)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

-   [html](/html/elements/html)

-   [i](/html/elements/i)

-   [img](/html/elements/img)

-   [input](/html/elements/input)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [legend](/html/elements/legend)

-   [mark](/html/elements/mark)

-   [option](/html/elements/option)

-   [p](/html/elements/p)

-   [samp](/html/elements/samp)

-   [script](/html/elements/script)

-   [span](/html/elements/span)

-   [strong](/html/elements/strong)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   [time](/html/elements/time)

### External resources

-   <http://www.w3.org/TR/html5/forms.html#attr-input-accept>

### Related pages (MSDN)

-   `input`
