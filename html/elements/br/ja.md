---
title: ja
tags:
  - Markup
  - Elements
  - HTML
  - XHTML
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Add Category, Parent, Children and Compatibility information. Modify DOM Interface information.'
summary: '文章をbreakするbr要素はテキストを強制的に終わらせ、brに続くテキストを新たしい行に改めます。'
code_samples:
  - 'http://gist.github.com/7282007'
uri: html/elements/br/ja
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/p/ja

---
# br

## Summary

文章をbreakするbr要素はテキストを強制的に終わらせ、brに続くテキストを新たしい行に改めます。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLBRElement](/dom/HTMLBRElement)

**br**要素は新しい段落を作らずに、強制的に現在のテキスト行を終わらせます。

**br**要素は詩や住所など、実際のコンテンツを区切るためだけに使われるべきで、一つの段落で論題のグループを区切るために使うものではありません。その場合は、[**paragraph**](/w/index.php?title=html/elements/p/ja&action=edit&redlink=1)要素.を使ってください。

**br**要素の中にどんなコンテンツ（属性など）を記述しようとも、周囲のテキストの一部とはみなされません。

## Examples

以下の例は**br**要素の正しい使い方を示しています。

``` {.html}
<p>P. シャーマン<br>
42 ワラビーウェイ<br>
シドニー</p>
```

[View live example](http://code.webplatform.org/gist/7282007)

## Usage

     br要素はコンテンツを持たない、タグ１つだけの”置換要素”です。classなどの属性を適用することはできますが、テキストを記述することはできません。

**br**は置換要素としてブラウザ側で自動的に閉じられますが、スラッシュを付けて明示的に閉じることもできます。

## Notes

閉じタグは不要です。

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-br-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-br-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-BR)
:   W3C Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [HTMLAudioElement](/dom/HTMLAudioElement)

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

-   **br**

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

<!-- -->

    … further results

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-synthesis](/css/properties/font-synthesis)

-   [hanging-punctuation](/css/properties/hanging-punctuation)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   [layout-flow](/css/properties/layout-flow)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [line-break](/css/properties/line-break)

-   [max-font-size](/css/properties/max-font-size)

-   [min-font-size](/css/properties/min-font-size)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [text-underline-position](/css/properties/text-underline-position)

-   [text-underline-style](/css/properties/text-underline-style)

-   [text-underline-width](/css/properties/text-underline-width)

-   [user-input](/css/properties/user-input)

-   [user-modify](/css/properties/user-modify)

-   [Text](/css/text)

-   [size](/html/attributes/size)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   **br**

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [em](/html/elements/em)

-   [font](/html/elements/font)

-   [hr](/html/elements/hr)

-   [i](/html/elements/i)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [mark](/html/elements/mark)

-   [samp](/html/elements/samp)

-   [strong](/html/elements/strong)

-   [Achieving typographic effects with the canvas tag](/tutorials/canvas_texteffects)

