---
title: ja
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
notes:
  - 'Add syntax, attribute, example, compatibility.'
summary: '<address>は文書や記事の所有者・著者とコンタクトをとるための情報を囲む要素です。'
uri: html/elements/address/ja
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/address/af
    - html/elements/address/ar
    - html/elements/address/ast
    - html/elements/address/az
    - html/elements/address/bcc
    - html/elements/address/bg
    - html/elements/address/br
    - html/elements/address/ca
    - html/elements/address/cs
    - html/elements/address/da
    - html/elements/address/de
    - html/elements/address/diq
    - html/elements/address/el
    - html/elements/address/eo
    - html/elements/address/es
    - html/elements/address/fa
    - html/elements/address/fi
    - html/elements/address/fr
    - html/elements/address/gl
    - html/elements/address/gu
    - html/elements/address/he
    - html/elements/address/hu
    - html/elements/address/hy
    - html/elements/address/id
    - html/elements/address/it
    - html/elements/address/ka
    - html/elements/address/kk
    - html/elements/address/km
    - html/elements/address/ko
    - html/elements/address/ksh
    - html/elements/address/kw
    - html/elements/address/mk
    - html/elements/address/ml
    - html/elements/address/mr
    - html/elements/address/ms
    - html/elements/address/nl
    - html/elements/address/no
    - html/elements/address/oc
    - html/elements/address/pl
    - html/elements/address/pt
    - html/elements/address/pt-br
    - html/elements/address/ro
    - html/elements/address/ru
    - html/elements/address/si
    - html/elements/address/sk
    - html/elements/address/sl
    - html/elements/address/sq
    - html/elements/address/sr
    - html/elements/address/sv
    - html/elements/address/ta
    - html/elements/address/th
    - html/elements/address/tr
    - html/elements/address/uk
    - html/elements/address/vi
    - html/elements/address/yue
    - html/elements/address/zh
    - html/elements/address/zh-hans
    - html/elements/address/zh-hant
    - html/elements/address/zh-tw

---
# address

## Summary

\<address\>は文書や記事の所有者・著者とコンタクトをとるための情報を囲む要素です。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

-   \<address\>要素は、addressと言っても住所情報を記載するためものではありません。（実際に関連する住所情報の場合は別ですが）
-   \<address\>には連絡を取るための情報以外の情報を記載してはいけません。
-   一般的に、\<address\>要素は\<footer\>要素の中で、他の情報の間に記載します。

## Examples

W3Cのサイトでは以下の様な連絡先情報を記載しています。

    <address>
        <p><a href="http://www.w3.org/Consortium/contact-mit">MIT</a></p>
    </address>

\<address\>要素の中に以下のような情報（最終更新日時など）を入れるのは正しくありません。

    <div>Last Modified: 1999/12/24 23:37:50</div>

## Notes

WebKit（safariや古いAndroid系）やTrident（Internet Explorer）では以下のようにデフォルトでスタイルが設定されています。

    address {
        display:block;
        font-style: italic;
    }

Gecko(Firefox)では以下のように設定されています。

    address, address[dir]{
             unicode-bidi: -moz-isolate;
             display:block;
             font-style:italic;
    }

### 標準情報

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 7.5.6

### HTML情報

Closing Tag
:   required
CSS Display
:   block

�

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-address-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/sections.html#the-address-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-ADDRESS)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

**言語:**
:   **[English](/html/elements/address)**  • <span lang="ja">**日本語**</span>
