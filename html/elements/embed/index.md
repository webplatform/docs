---
title: 'EMBED'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: embed
  topic: html
notes:
  - "Add history of the element\nAdd Category, Parent, Children and Compatibility information."
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLEmbedElement](/dom/HTMLEmbedElement)'
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'The HTML &lt;embed&gt; Element represents an integration point for an external content- typically, non-HTML content such as an application or some other type of interactive content which involves use of a third-party plugin as a handler (rather than being natively supported by the UA).'
tags:
  - Markup_Elements
  - Audio
  - HTML
  - Media
  - Video
uri: html/elements/embed

---
## Summary

The HTML &lt;embed&gt; Element represents an integration point for an external content- typically, non-HTML content such as an application or some other type of interactive content which involves use of a third-party plugin as a handler (rather than being natively supported by the UA).

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLEmbedElement](/dom/HTMLEmbedElement)

## Accessibility

Authors should ensure that the information and user interface components must be presentable to users in ways they can perceive ([WCAG 2.0 - Principle 1: Perceivable](http://www.w3.org/TR/WCAG20/#perceivable)). This includes providing alternatives for time-based media [Guideline 1.2](http://www.w3.org/TR/WCAG20/#media-equiv).

## HTML Attributes

-   `src` = URL potentially surrounded by spaces
    gives the address of the resource being embedded.
-   `type` = MIME type
    Specifies the type of the resource.
-   `width` = non-negative integer
    Give the width of the visual content of the element, in CSS pixels.
-   `height` = non-negative integer
    Give the height of the visual content of the element, in CSS pixels.

## History

While only being formalized as of HTML5, the tag has been informally supported among some user-agents as far back as Netscape Navigator 2.0 [[1]](http://lists.w3.org/Archives/Public/www-talk/1995SepOct/0045.html)

## Examples

The following use of the **EMBED** element mimics the behavior of the **BGSOUND** tag.

``` html
<EMBED type="audio/x-midi" src="BackInTheSaddle.mid" hidden="true">
```

Way to embed a resource that requires a proprietary plugin, like Flash.If the user does not have the plugin (for example if the plugin vendor doesn't support the user's platform), then the user will be unable to use the resource.

``` html
<Embed src="catgame.swf">
```

To pass the plugin a parameter "quality" with the value "high", an attribute can be specified:

``` html
<Embed src="catgame.swf" quality="high">
```

## Usage

     The interactive element embed must not appear as a descendant of the a element.

The interactive element embed must not appear as a descendant of the button element. The name attribute on the embed element is obsolete. Use the id attribute instead. The align attribute on the embed element is obsolete. Use CSS instead. The hspace attribute on the embed element is obsolete. Use CSS instead. The vspace attribute on the embed element is obsolete. Use CSS instead.

## Notes

### Remarks

The **EMBED** element must appear inside the **BODY** element of the document. Users need to have an application that can view the data installed on their computer. **Tip:  ** In some cases, you may achieve better results by adding the file name extension of the add-on as a query parameter to the file name specified in the [**SRC**](/html/attributes/src_(iframe,_embed,_xml)) attribute.

Permitted attributes - global attributes,& src ,& type, & height, & width, & Any other attribute that has no namespace.

Permitted parent elements Any element that can contain phrasing elements

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-embed-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-embed-element)
:   W3C Recommendation

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

-   **EMBED**

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

-   [standby](/html/attributes/standby)

-   **EMBED**

-   [img](/html/elements/img)

-   [WebRTC Resources](/tutorials/webrtc_resources)

#### Video

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [object-fit](/css/properties/object-fit)

-   **EMBED**

-   [video](/html/elements/video)

-   [MSEPrimer](/tutorials/MSEPrimer)

-   [HTML5 Video and Other Recommendations](/tutorials/video_others)

-   [WebRTC Resources](/tutorials/webrtc_resources)
