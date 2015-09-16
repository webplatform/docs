---
title: article
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
lang: ja
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: '&lt;article&gt;はページ内で単独で完結する構成要素を定義します。'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/article/af
    - html/elements/article/ar
    - html/elements/article/ast
    - html/elements/article/az
    - html/elements/article/bcc
    - html/elements/article/bg
    - html/elements/article/br
    - html/elements/article/ca
    - html/elements/article/cs
    - html/elements/article/da
    - html/elements/article/de
    - html/elements/article/diq
    - html/elements/article/el
    - html/elements/article/eo
    - html/elements/article/es
    - html/elements/article/fa
    - html/elements/article/fi
    - html/elements/article/fr
    - html/elements/article/gl
    - html/elements/article/gu
    - html/elements/article/he
    - html/elements/article/hu
    - html/elements/article/hy
    - html/elements/article/id
    - html/elements/article/it
    - html/elements/article/ka
    - html/elements/article/kk
    - html/elements/article/km
    - html/elements/article/ko
    - html/elements/article/ksh
    - html/elements/article/kw
    - html/elements/article/mk
    - html/elements/article/ml
    - html/elements/article/mr
    - html/elements/article/ms
    - html/elements/article/nl
    - html/elements/article/no
    - html/elements/article/oc
    - html/elements/article/pl
    - html/elements/article/pt
    - html/elements/article/pt-br
    - html/elements/article/ro
    - html/elements/article/ru
    - html/elements/article/si
    - html/elements/article/sk
    - html/elements/article/sl
    - html/elements/article/sq
    - html/elements/article/sr
    - html/elements/article/sv
    - html/elements/article/ta
    - html/elements/article/th
    - html/elements/article/tr
    - html/elements/article/uk
    - html/elements/article/vi
    - html/elements/article/yue
    - html/elements/article/zh
    - html/elements/article/zh-hans
    - html/elements/article/zh-hant
    - html/elements/article/zh-tw
    - html/elements/nav/ja
uri: html/elements/article/ja

---
## Summary

&lt;article&gt;はページ内で単独で完結する構成要素を定義します。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

\<article\>は\<div\>タグを減らすためにHTML5から導入された要素です。**\<article\>**は主に以下の内容を表します。

-   フォーラムの投稿
-   雑誌や新聞の記事
-   ブログのエントリ
-   ユーザの投稿したコメント
-   インタラクティブなウィジェット/ガジェット

上記以外にも独立したコンテンツを表すのに使います。

**\<article\>**要素をネストする時は、内側の\<article\>の内容は外側の\<article\>に関連したコンテンツでなければいけません。例えば、コメントの付いたブログのエントリでは、ブログエントリの**\<article\>**の中にコメントの**\<article\>**をネストするほうがよいでしょう。

## Examples

以下の例では**\<article\>**、**\<header\>**、**\<footer\>**を使った記事の基本構成を示します。

``` html
<article>
 <header>
  <h1>見出し</h1>
 </header>
 <p>本文</p>
 <p>...</p>
 <footer>フッター</footer>
</article>
```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-article-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/sections.html#the-article-element)
:   W3C Recommendation

## See also

### Other articles

[nav](/w/index.php?title=html/elements/nav/ja&action=edit&redlink=1) - \<article\>タグの子要素としてよく用いられます。

### External resources

-   <http://www.w3.org/TR/html-markup/article.html#article>

