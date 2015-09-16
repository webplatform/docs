---
title: 'rt'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rt.htm'
compatibility:
  feature: rt
  topic: html
notes:
  - 'HTML information section must be modified. Add compatibility and more example.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
summary: 'The rt element marks the ruby text component of a ruby annotation.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/rt

---
## Summary

The rt element marks the ruby text component of a ruby annotation.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

Internationalization topics related to the `rt` element:

-   [Using ruby markup](http://localhost/International/techniques/authoring-html#ruby)

## Examples

This example uses the **RT** element to specify a string of text as an annotation or pronunciation guide to the base text.

``` html
<ruby>
   Base Text
   <rt>Ruby Text
</ruby>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rt.htm)

``` html

<p lang="ja">...<ruby>漢<rt>かん</rt>字<rt>じ</rt></ruby>...</p>

```

## Notes

### Remarks

A ruby is an annotation or pronunciation guide for a string of text. The string of text annotated with a ruby is referred to as the base. The ruby text specified by the **RT** element is positioned **above** or **inline** with the [**rubyPosition**](/css/properties/ruby-position) property. Browsers that do not support the **RT** element render the ruby text inline with the base text. This element is available in HTML and script as of Microsoft Internet Explorer 5. The ruby text specified by the **RT** element is positioned **above** or **inline** with the [**rubyPosition**](/css/properties/ruby-position) property.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-rt-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-rt-element)
:   W3C Recommendation

## See also

### Related pages

-   `ruby`
