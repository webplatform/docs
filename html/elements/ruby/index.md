---
title: 'ruby'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ruby.htm'
compatibility:
  feature: ruby
  topic: html
notes:
  - 'HTML information section must be modified. Add compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The ruby element allows one or more spans of phrasing content to be marked with ruby annotations. Ruby annotations are short runs of text presented alongside base text, primarily used in East Asian typography as a guide for pronunciation or to include other annotations.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/ruby

---
## Summary

The ruby element allows one or more spans of phrasing content to be marked with ruby annotations. Ruby annotations are short runs of text presented alongside base text, primarily used in East Asian typography as a guide for pronunciation or to include other annotations.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

Ruby annotations are short runs of text presented alongside base text, primarily used in East Asian typography as a guide for pronunciation or to include other annotations.

In Japanese, this form of typography is also known as *furigana*.

## Examples

This example uses the **RUBY** element to specify the first string of text as the base, and the **RT** element to specify the second string of text as the ruby.

``` html

<ruby>
  <rb>Base Text</rb>
  <rt>Ruby Text</rt>
</ruby>

```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ruby.htm)

In this example, each ideograph in the Japanese text *漢字* is annotated with its reading in *hiragana*.

``` html

<p lang="ja">...<ruby>漢<rt>かん</rt>字<rt>じ</rt></ruby>...</p>

```

## Notes

### Remarks

A ruby is an annotation or pronunciation guide for a string of text. The string of text annotated with a ruby is referred to as the base. The only valid object within the **RUBY** element is the **RT** element. Text not contained within the ruby text object, **RT**, is assumed to be a part of the base. This element is available in HTML and script as of Microsoft Internet Explorer 5.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-ruby-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-ruby-element)
:   W3C Recommendation

## See also

### Related articles

#### Ruby

-   [Ruby](/css/ruby)

-   **ruby**

### External resources

-   [Using ruby markup](http://www.w3.org/International/techniques/authoring-html#ruby)

### Related pages

-   `rt`
