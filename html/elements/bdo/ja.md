---
title: 'bdo'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: ja
  topic: html
lang: ja
notes:
  - 'Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
summary: 'bdo要素はページ上のテキスト表記の方向を定義することができます。（”BDO”とはBi-Directional Override（双方向オーバーライド）の略です。）'
tags:
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/attributes/dir/ja
uri: html/elements/bdo/ja

---
## Summary

bdo要素はページ上のテキスト表記の方向を定義することができます。（”BDO”とはBi-Directional Override（双方向オーバーライド）の略です。）

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

`bdo`に関連する国際化トピック:

-   [Overriding the Unicode bidirectional algorithm](http://www.w3.org/International/techniques/authoring-html#bdo)
-   [Mixing text direction inline](http://www.w3.org/International/techniques/authoring-html#inline)

## Examples

ここではテキストを正しく読める向きに表示するために**bdo**要素を使います。

以下のテキストには英語のように左から右に書いた文字列とヘブライ語のように右から左に書いた文字列が含まれています。

この文は英語です、すで語イラブヘは文のこ。 （「すで語イラブヘは文のこ」はひっくり返っていますが、ヘブライ語として正しい向きで表示されていると考えてください。）

この文章に対してUnicodeの双方向アルゴリズムを適用しようとする場合、テキストは2回ひっくり返されて右から左ではなく左から右に、正しくないない表示になってしまいます。ここで正しく読める順番で書いたテキストを[**dir**](/w/index.php?title=html/attributes/dir/ja&action=edit&redlink=1)属性に**ltr**を指定した**bdo**タグの間に記述することで双方向アルゴリズムを無効化することができます。

``` html
<BDO DIR="ltr">この文は英語です、
    すで語イラブヘは文のこ。</BDO>
```

## Notes

### 備考

Unicodeの双方向アルゴリズムでは文字列はもともと埋め込まれていた方向に自動的に変換されますが、**bdo**要素ではテキストの表示方向を制御することができます。

例えば、英語文書は基本的に左から右(ltr)に書かれます。 しかし、右から左(rtl)に書かれる言語を含む文節がドキュメント内にある場合、双方向アルゴリズムを用いて方向を変換しなければいけません。 通常埋め込まれた方向を変えるのには双方向アルゴリズムと[**dir**](/html/attributes/dir)属性で十分です。 しかし双方向アルゴリズムで、フォーマットされたテキストを表示しようとしても、正しく表示されない場合があります。 例えば、英語とヘブライ語を含む段落で正しく逆方向にされていないメールアドレスなどがある場合などです。 これはメールアドレスが双方向アルゴリズムによってヘブライ語の方向で2回逆にされるためです。

bdo要素は双方向アルゴリズムを無効化し、表示順を制御します。 bdo要素を使う上で[**dir**](/html/attributes/dir)属性は必須です。 bdo要素はInternet Explorer 5以上で利用可能です。

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-bdo-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-bdo-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/dirlang.html#edef-BDO)
:   W3C Recommendation

## See also

### Related pages

-   direction[direction](/css/properties/direction)
