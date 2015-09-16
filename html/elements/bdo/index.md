---
title: bdo
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
summary: 'The bdo element (&lt;bdo&gt;) allows you to specify the direction in which text is to be rendered on the page. (&quot;BDO&quot; stands for Bi-Directional Override.)'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/bdo

---
## Summary

The bdo element (&lt;bdo&gt;) allows you to specify the direction in which text is to be rendered on the page. (&quot;BDO&quot; stands for Bi-Directional Override.)

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

Internationalization topics related to the `bdo` element:

-   [Overriding the Unicode bidirectional algorithm](http://www.w3.org/International/techniques/authoring-html#bdo)
-   [Mixing text direction inline](http://www.w3.org/International/techniques/authoring-html#inline)

## Examples

This example uses the **BDO** element to correct the reading order of a block of text.

The following string includes text written in the left-to-right order of the English language and the right-to-left order of Hebrew: This fragment is in English, WERBEH NI SI TNEMGARF SIHT.

Assume that the right-to-left text (WERBEH NI SI TNEMGARF SIHT.) already has been inverted, so that it displays in the correct direction. If you subsequently apply the Unicode bidirectional to the text, the text inverts a second time and incorrectly displays as left-to-right instead of right-to-left.

``` html
<BDO DIR="ltr">This fragment is in English,
    WERBEH NI SI TNEMGARF SIHT.</BDO>
```

[The solution is to override the bidirectional algorithm and put the block of text in the correct reading order inside a **BDO** element whose [**DIR**](/html/attributes/dir) attribute is set to **ltr**. View live example]

## Notes

### Remarks

The **BDO** element can be used to control the reading order of a block of text. The Unicode bidirectional algorithm automatically reverses embedded character sequences according to their inherent direction. For example, the base direction of an English document is left-to-right (ltr). If portions of a paragraph within this document contain a language with the right-to-left (rtl) reading order, you can reverse the direction of that language by applying the bidirectional algorithm. The bidirectional algorithm and the [**DIR**](/html/attributes/dir) attribute generally suffice for embedded direction changes. However, incorrect presentations can occur when you expose formatted text to the bidirectional algorithm. For example, a paragraph containing English and Hebrew that is formatted for e-mail could be incorrectly inverted by the bidirectional algorithm. Because the reading order of the Hebrew text was inverted once for the e-mail, exposing it to the bidirectional algorithm would invert the words a second time. The **BDO** element turns off the algorithm and controls the reading order. The [**DIR**](/html/attributes/dir) attribute is required when you use the **BDO** element. This element is available in HTML and script as of Microsoft Internet Explorer 5.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-bdo-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-bdo-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/dirlang.html#edef-BDO)
:   W3C Recommendation

## See also

### Related pages (MSDN)

-   `direction`
