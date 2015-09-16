---
title: 'b'
code_samples:
  - 'http://gist.github.com/7281844'
  - 'http://gist.github.com/321e5149c1e661e1de14'
compatibility:
  feature: ja
  topic: html
lang: ja
notes:
  - 'Add compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: '&lt;b&gt;要素は特に重要であることを伝えるのに使うものではなく、あくまで通常の文章において文体的にテキストを強調する際に使用します。'
tags:
  - Markup
  - Elements
  - HTML
  - XHTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/b/af
    - html/elements/b/ar
    - html/elements/b/ast
    - html/elements/b/az
    - html/elements/b/bcc
    - html/elements/b/bg
    - html/elements/b/br
    - html/elements/b/ca
    - html/elements/b/cs
    - html/elements/b/da
    - html/elements/b/de
    - html/elements/b/diq
    - html/elements/b/el
    - html/elements/b/eo
    - html/elements/b/es
    - html/elements/b/fa
    - html/elements/b/fi
    - html/elements/b/fr
    - html/elements/b/gl
    - html/elements/b/gu
    - html/elements/b/he
    - html/elements/b/hu
    - html/elements/b/hy
    - html/elements/b/id
    - html/elements/b/it
    - html/elements/b/ka
    - html/elements/b/kk
    - html/elements/b/km
    - html/elements/b/ko
    - html/elements/b/ksh
    - html/elements/b/kw
    - html/elements/b/mk
    - html/elements/b/ml
    - html/elements/b/mr
    - html/elements/b/ms
    - html/elements/b/nl
    - html/elements/b/no
    - html/elements/b/oc
    - html/elements/b/pl
    - html/elements/b/pt
    - html/elements/b/pt-br
    - html/elements/b/ro
    - html/elements/b/ru
    - html/elements/b/si
    - html/elements/b/sk
    - html/elements/b/sl
    - html/elements/b/sq
    - html/elements/b/sr
    - html/elements/b/sv
    - html/elements/b/ta
    - html/elements/b/th
    - html/elements/b/tr
    - html/elements/b/uk
    - html/elements/b/vi
    - html/elements/b/yue
    - html/elements/b/zh
    - html/elements/b/zh-hans
    - html/elements/b/zh-hant
    - html/elements/b/zh-tw
    - html/elements/span/ja
    - html/elements/strong/ja
    - html/elements/dfn/ja
    - html/elements/hn/ja
    - html/elements/abbr/ja
uri: html/elements/b/ja

---
## Summary

&lt;b&gt;要素は特に重要であることを伝えるのに使うものではなく、あくまで通常の文章において文体的にテキストを強調する際に使用します。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

\<b\>要素は通常、ブラウザ上でテキストを太字で表示するのに使われます。多くのブラウザで広くサポートされていますが、CSSでより意味的に適切な要素で全く同じ効果を表現できるため、太字にするという目的のために**\<b\>**要素を使用するのは推奨されていません。HTML5では、**\<b\>**要素の意味が再定義され、他のテキストと区別するために使われるようになりました。周囲のテキストよりも重要であるという意味はもうありません。

\<b\>要素は他に適切な要素がない場合の最終手段として使うようにしてください。そのテキストがスタイル的に重要だと示されている以外の意味はありません（[**span** 要素](/w/index.php?title=html/elements/span/ja&action=edit&redlink=1)の省略形とい言ってもいいでしょう）。意味があり、似たような効果をもたらす要素として、[strong](/w/index.php?title=html/elements/strong/ja&action=edit&redlink=1)、[dfn](/w/index.php?title=html/elements/dfn/ja&action=edit&redlink=1)、[h1-h6](/w/index.php?title=html/elements/hn/ja&action=edit&redlink=1)、[abbr](/w/index.php?title=html/elements/abbr/ja&action=edit&redlink=1).があります。

## Examples

以下の例では、アドベンチャーゲームのテキストの特別な部分を**\<b\>**要素を使って強調しています。

``` html
<p>あなたは小さな部屋に入りました。
するとあなたの<b>剣</b>が眩しく輝き始めました。
<b>ネズミ</b>は壁の隅をちょこまかと走って行きました。</p>
```

[View live example](http://code.webplatform.org/gist/7281844)

こちらの例では、**\<b\>**要素を使って社名と製品名を強調しています。CSSの曖昧さ回避のため、**class**属性を使用しています。

``` html
<p><b class="org">Acme <abbr title="Corporation">Corp</abbr></b>は<b class="product">ウィジェットブラスト3000</b>を紹介することができ、とても嬉しく思っています。
これは朝卵を焼くところから夜子供を寝かしつけるまで、あなたの生活を楽にする現代科学の奇跡です。</p>
```

[View live example](http://code.webplatform.org/gist/321e5149c1e661e1de14)

## Usage

     <b>要素は人名、社名、製品名、地名などの固有名詞を囲んで、周囲のテキストと区別するために使いますが、意味という意味はありません。

**\<b\>**要素に関連する国際化トピック

-   [[b and i tags](http://www.w3.org/International/techniques/authoring-html#bandi%7CUsing)]

## Notes

**\<b\>**要素は意味を持たないため、自分で意味を持たせて使ってはいけません。もっと適切な要素があるはずです。見出しには**\<h1\>**～**\<h6\>**要素を、アクセントを付けたい場合は**\<em\>**要素を、重要性を示すには**\<strong\>**要素を、文脈上重要/強調したいテキストには**\<mark\>**要素を使うべきでしょう。

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-b-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-b-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/present/graphics.html#edef-B)
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

-   **b**

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

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-modify](/css/properties/user-modify)

-   [Text](/css/text)

-   [size](/html/attributes/size)

-   [b](/html/elements/b)

-   **b**

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

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
