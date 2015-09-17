---
title: 'alt'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: alt
  topic: html
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The alt attribute is used as a textual representation for graphics and buttons in browsers that don''t or can''t render images, or when the resource is not found.'
tags:
  - Markup_Attributes
  - Accessibility
  - HTML
  - Media
  - Usability
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/input/image
    - aria/attributes/aria-label
uri: html/attributes/alt

---
## Summary

The alt attribute is used as a textual representation for graphics and buttons in browsers that don't or can't render images, or when the resource is not found.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[HTMLImageElement](/dom/HTMLImageElement)

</td>
</tr>
</table>
The **alt** attribute is required for [images](/html/elements/img) and [image buttons](/w/index.php?title=html/elements/input/image&action=edit&redlink=1). It should provide a concise and accurate label representing the image, in case that a user is visually disabled, is using browser that doesn’t render images or can’t receive images due to network errors. If no alt attribute is given, a screen reader can only read “image” or the file name, which is especially bad if the image is the sole content of a link.

The alt text should be useful in the context it’s displayed. Which alt text is useful, depends on the function of the image on the page. The content of an alt attribute should use general, non-visual language to accommodate non visual users. For example, a picture of a lake intended to evoke an emotion should have text more descriptive than "Lake" or "Clear, blue lake". "Breathtaking open lake" may be more appropriate.

If an image is not intended to be part of the content of the page, but instead is purely decorative, the alt text can be an empty string. This case could apply for an image used as a border or spacing element or if the image is redundantly described in “regular” text on the page.

If the image contains (non-decorative) text, that text should be in the alternative text in full.

## Examples

In this example the images provice important information. The alt text therefore needs to convey the same content.

``` html
<p>We accept the these credit cards:</p>
<ul>
   <li><img src="visa.png" alt="Visa"></li>
   <li><img src="americanexpress.png" alt="American Express"></li>
</ul>
```

Depending on the context, the alt text can be short and simple or more descriptive:

``` html
<img src="capitol.jpg" alt="The Capitol">

<img src="capitol.jpg" alt="Capital Dome in neo Classical style. Dome is white, circular with narrow windows on many levels and pillars on the lowest level.">
```

This example shows a decorative use of an image:

``` html
<img src="border.png" alt="">
```

This example shows a redundant image in a link:

``` html
<a href="crocuspage.html">
    <img src="crocus.jpg" alt="">
    <strong> Crocus bulbs</strong>
</a>
```

This example shows a image that is used as a functional icon. A non-empty alt text is mandatory in such cases.

``` html
<a href="javascript:print()">
    <img src="print.png" alt="Print this page">
</a>
```

## Related specifications

[HTML5](http://www.w3.org/TR/html5/embedded-content-0.html#alt)
:   Proposed Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   **alt**

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

### Other articles

Other attributes that can convey alternative text or longer descriptions:

-   [aria/attributes/aria-label](/w/index.php?title=aria/attributes/aria-label&action=edit&redlink=1)
-   [aria/attributes/aria-labelledby](/aria/attributes/aria-labelledby)

-   [html/attributes/longDesc](/html/attributes/longDesc)
-   [aria/attributes/aria-describedby](/aria/attributes/aria-describedby)

### External resources

-   [W3C WAI Web Accessibility Tutorial on Images](http://www.w3.org/WAI/tutorials/images/)
-   [W3C WAI Web Accessibility Tutorial **alt decision tree**](http://www.w3.org/WAI/tutorials/images/decision-tree/)
-   <http://www.w3.org/TR/2012/WD-html-alt-techniques-20120329/#secm1>
-   <http://www.w3.org/TR/html5/forms.html#attr-input-alt>
