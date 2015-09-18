---
title: 'width'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/7283238'
  - 'https://code.webplatform.org/gist/dbe042fac0e620a8f2b4'
compatibility:
  feature: width
  topic: html
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies the width, in pixels, of certain content elements.'
tags:
  - Markup_Attributes
  - HTML
uri: html/attributes/width

---
## Summary

Specifies the width, in pixels, of certain content elements.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[HTMLImgElement](/html/elements/img)

</td>
</tr>
</table>
The **width** attribute specifies the visual width of [img](/html/elements/img), [iframe](/html/elements/iframe), [embed](/html/elements/embed), [object](/html/elements/object), [video](/html/elements/video), [canvas](/html/elements/canvas), and [input[type="image"]](/html/elements/input/type/image) in pixels.

By default, elements will not preserve aspect ratio when width attribute is set, without a height attribute. If a width attribute is set, but no height, an image will scale to preserve its original aspect ratio. If both the width and height are zero, the element should not be intended to be visible by the user.

Width values must be non-negative integers.

## Examples

\<img\> with width attribute.

``` html
<img src="http://www.webplatform.org/logo/wplogo_transparent_xlg.png" height="100" width="150">
```

[View live example](http://code.webplatform.org/gist/7283238)

\<canvas\> with width attribute

``` html
<canvas width="200" height="200"></canvas>
```

[View live example](https://code.webplatform.org/gist/dbe042fac0e620a8f2b4)

## Related specifications

[HTML4 Specification](http://www.w3.org/TR/html401/)
:   W3C Recommendation
