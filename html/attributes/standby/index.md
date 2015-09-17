---
title: 'standby'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[[1]](https://developer.mozilla.org/en-US/docs/HTML/Element/object) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: standby
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'A message for the browser to show while an object''s implementation and data load.'
tags:
  - Markup_Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLElement/object
uri: html/attributes/standby

---
## Summary

A message for the browser to show while an object's implementation and data load.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[dom/HTMLElement/object](/w/index.php?title=dom/HTMLElement/object&action=edit&redlink=1)

</td>
</tr>
</table>
A message for the browser to show while an `object`'s implementation and data load.

## Examples

The `standby` attribute used to alert users to a lengthy delay before the image displays.

``` html
<object data="huge-picture.png" standby="Loading...">
</object>
```

## Notes

### Remarks

This property has no default value.

Windows Internet Explorer does not render the **standby** message while loading an object's implementation or data; however, some objects may react to or display the content of this string.

**standby** was introduced in Microsoft Internet Explorer 6

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## Related specifications

[HTML5 differences from HTML4: Obsolete Attributes](http://dev.w3.org/html5/html4-differences/#obsolete-attributes)
:   Editor's Draft

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

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

-   **standby**

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

#### Multimedia

-   [Track ended](/apis/MediaStream/ended)

-   [MediaSource](/apis/media_source_extensions/MediaSource)

-   [appendBuffer](/apis/media_source_extensions/MediaSource/appendBuffer)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [object-fit](/css/properties/object-fit)

-   [height](/html/attributes/height)

-   **standby**

-   [EMBED](/html/elements/embed)

-   [img](/html/elements/img)

-   [WebRTC Resources](/tutorials/webrtc_resources)

### External resources

-   <http://dev.w3.org/html5/html4-differences/>
-   <http://reference.sitepoint.com/html/object/standby>

### Related pages

-   `object`
