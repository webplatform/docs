---
title: !DOCTYPE
lang: ja
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
summary: '文書型宣言（DOCTYPE宣言）とはSGMLやXML文書(webページなど)を文書型定義(DTD)(HTMLのバージョンごとの書式の定義など）と結びつけるためのものです。ドキュメントをシリアライズした書式中で、特定の構文にマッチするようにマークアップした短い文字列で指定します。&lt;!DOCTYPE&gt;を書かないとQuirksモード(互換モード)で表示されます。'
tags:
  - Markup
  - Elements
  - DOCTYPE
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/!DOCTYPE/af
    - html/elements/!DOCTYPE/ar
    - html/elements/!DOCTYPE/ast
    - html/elements/!DOCTYPE/az
    - html/elements/!DOCTYPE/bcc
    - html/elements/!DOCTYPE/bg
    - html/elements/!DOCTYPE/br
    - html/elements/!DOCTYPE/ca
    - html/elements/!DOCTYPE/cs
    - html/elements/!DOCTYPE/da
    - html/elements/!DOCTYPE/de
    - html/elements/!DOCTYPE/diq
    - html/elements/!DOCTYPE/el
    - html/elements/!DOCTYPE/eo
    - html/elements/!DOCTYPE/es
    - html/elements/!DOCTYPE/fa
    - html/elements/!DOCTYPE/fi
    - html/elements/!DOCTYPE/fr
    - html/elements/!DOCTYPE/gl
    - html/elements/!DOCTYPE/gu
    - html/elements/!DOCTYPE/he
    - html/elements/!DOCTYPE/hu
    - html/elements/!DOCTYPE/hy
    - html/elements/!DOCTYPE/id
    - html/elements/!DOCTYPE/it
    - html/elements/!DOCTYPE/ka
    - html/elements/!DOCTYPE/kk
    - html/elements/!DOCTYPE/km
    - html/elements/!DOCTYPE/ko
    - html/elements/!DOCTYPE/ksh
    - html/elements/!DOCTYPE/kw
    - html/elements/!DOCTYPE/mk
    - html/elements/!DOCTYPE/ml
    - html/elements/!DOCTYPE/mr
    - html/elements/!DOCTYPE/ms
    - html/elements/!DOCTYPE/nl
    - html/elements/!DOCTYPE/no
    - html/elements/!DOCTYPE/oc
    - html/elements/!DOCTYPE/pl
    - html/elements/!DOCTYPE/pt
    - html/elements/!DOCTYPE/pt-br
    - html/elements/!DOCTYPE/ro
    - html/elements/!DOCTYPE/ru
    - html/elements/!DOCTYPE/si
    - html/elements/!DOCTYPE/sk
    - html/elements/!DOCTYPE/sl
    - html/elements/!DOCTYPE/sq
    - html/elements/!DOCTYPE/sr
    - html/elements/!DOCTYPE/sv
    - html/elements/!DOCTYPE/ta
    - html/elements/!DOCTYPE/th
    - html/elements/!DOCTYPE/tr
    - html/elements/!DOCTYPE/uk
    - html/elements/!DOCTYPE/vi
    - html/elements/!DOCTYPE/yue
    - html/elements/!DOCTYPE/zh
    - html/elements/!DOCTYPE/zh-hans
    - html/elements/!DOCTYPE/zh-hant
    - html/elements/!DOCTYPE/zh-tw
uri: html/elements/!DOCTYPE/ja

---
## <span>Summary</span>

文書型宣言（DOCTYPE宣言）とはSGMLやXML文書(webページなど)を文書型定義(DTD)(HTMLのバージョンごとの書式の定義など）と結びつけるためのものです。ドキュメントをシリアライズした書式中で、特定の構文にマッチするようにマークアップした短い文字列で指定します。&lt;!DOCTYPE&gt;を書かないとQuirksモード(互換モード)で表示されます。

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## <span>Examples</span>

HTML5ではDOCTYPE宣言は以下のように記述されます。

``` html
<!DOCTYPE html>
```

HTML4.01のStrict DTDでは

``` html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
```

HTML4.01のTransitional DTDでは

``` html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

## <span>Usage</span>

     htmlファイルの始まりの部分に

``` html
<!DOCTYPE html>
```

    を追加してください。

## <span>Notes</span>

\<!DOCTYPE\>はHTML文書の\<html\>タグより前の一番最初の部分に書かなければいけません。

\<!DOCTYPE\>はHTMLのタグではなく、ブラウザにそのhtmlファイルのバージョン情報を教えるためのものです。

HTML4.01はSGMLベースであり、\<!DOCTYPE\>では参照するDTDを指定します。 DTDがマークアップ言語用のルールを定義しているため、ブラウザはコンテンツを正しく表示することができます。

一方HTML5はSGMLベースではないため、DTDを参照する必要がありません。

## <span>See also</span>

### <span>Related articles</span>

#### <span>Deprecated</span>

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

-   [MutationEvent](/dom/MutationEvent)

-   [attrChange](/dom/MutationEvent/attrChange)

-   [attrName](/dom/MutationEvent/attrName)

-   [initMutationEvent](/dom/MutationEvent/initMutationEvent)

-   [newValue](/dom/MutationEvent/newValue)

-   [prevValue](/dom/MutationEvent/prevValue)

-   [relatedNode](/dom/MutationEvent/relatedNode)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   **!DOCTYPE**

-   [acronym](/html/elements/acronym)

-   [escape](/javascript/escape)

-   [unescape](/javascript/unescape)

#### <span>HTML</span>

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

-   **!DOCTYPE**

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

### <span>Other articles</span>

html/quirksmode

と記述されます。