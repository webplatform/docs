---
title: 'base'
compatibility:
  feature: ja
  topic: html
lang: ja
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLBaseElement](/dom/HTMLBaseElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: '&lt;base&gt;は文書の基準となるURLを明示し、文書内の相対URLを解決するために使用します。.'
tags:
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/base/af
    - html/elements/base/ar
    - html/elements/base/ast
    - html/elements/base/az
    - html/elements/base/bcc
    - html/elements/base/bg
    - html/elements/base/br
    - html/elements/base/ca
    - html/elements/base/cs
    - html/elements/base/da
    - html/elements/base/de
    - html/elements/base/diq
    - html/elements/base/el
    - html/elements/base/eo
    - html/elements/base/es
    - html/elements/base/fa
    - html/elements/base/fi
    - html/elements/base/fr
    - html/elements/base/gl
    - html/elements/base/gu
    - html/elements/base/he
    - html/elements/base/hu
    - html/elements/base/hy
    - html/elements/base/id
    - html/elements/base/it
    - html/elements/base/ka
    - html/elements/base/kk
    - html/elements/base/km
    - html/elements/base/ko
    - html/elements/base/ksh
    - html/elements/base/kw
    - html/elements/base/mk
    - html/elements/base/ml
    - html/elements/base/mr
    - html/elements/base/ms
    - html/elements/base/nl
    - html/elements/base/no
    - html/elements/base/oc
    - html/elements/base/pl
    - html/elements/base/pt
    - html/elements/base/pt-br
    - html/elements/base/ro
    - html/elements/base/ru
    - html/elements/base/si
    - html/elements/base/sk
    - html/elements/base/sl
    - html/elements/base/sq
    - html/elements/base/sr
    - html/elements/base/sv
    - html/elements/base/ta
    - html/elements/base/th
    - html/elements/base/tr
    - html/elements/base/uk
    - html/elements/base/vi
    - html/elements/base/yue
    - html/elements/base/zh
    - html/elements/base/zh-hans
    - html/elements/base/zh-hant
    - html/elements/base/zh-tw
    - dom/Location/ja
    - html/attributes/href/ja
    - html/elements/form/ja
    - html/attributes/target/ja
    - html/elements/iframe/ja
uri: html/elements/base/ja

---
## Summary

&lt;base&gt;は文書の基準となるURLを明示し、文書内の相対URLを解決するために使用します。.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLBaseElement](/dom/HTMLBaseElement)

<table class="wikitable">
<tr>
<th style="vertical-align: top" id="permitted-contents">
Permitted contents

</th>
<td style="vertical-align: top; padding-top: 10px">
*なし*

</td>
</tr>
<tr>
<th id="permitted-parents">
Permitted parents

</th>
<td>
[`<head>`](/html/elements/head)タグ内で1度のみ許可されています。

</td>
</tr>
</table>
アクセスする前に相対URL（<var>some/example.html</var>）を絶対URL(<var><http://example.org/some/example.html></var>) に変換しなければいけません。通常、相対URLを解決するためのベースURLとしてそのドキュメントのURL（JavaScriptで使用する[`location`](/w/index.php?title=dom/Location/ja&action=edit&redlink=1)オブジェクト）が使用されます。\<base\>要素の[`href`](/w/index.php?title=html/attributes/href/ja&action=edit&redlink=1)属性を記述することでデフォルトのベースURLを上書く事ができます。

リンク([`<a>`](/html/elements/a/ja))やフォーム([`<form>`](/w/index.php?title=html/elements/form/ja&action=edit&redlink=1))で[`target`](/w/index.php?title=html/attributes/target/ja&action=edit&redlink=1)を開きますが、デフォルトのtargetは<var>\_self</var>で、現在ドキュメントを表示しているのと同じウィンドウでリンクを開くことになります。`<base target="…">`と書くことでドキュメント全体のtargetのデフォルトを上書くことができます。

ドキュメントが[`iframe`](/w/index.php?title=html/elements/iframe/ja&action=edit&redlink=1)を使って構成されている場合、`<base target="_parent">`と設定することで親フレームでリンクを開くことができます。フレームを使っていないドキュメントで<var>\_parent</var>や<var>\_top</var>を使用する場合、<var>\_self</var>と同じ動きになります。

## HTML属性

-   `href`= URI（前後のスペースは取り除かれます。）
    href属性を指定した\<base\>要素は、URLを使う属性を持つ他の要素よりも前に記述しなければいけません。（\<html\>要素以外。manifest属性はbase要素の影響を受けないため。）[[Example A]](#Example_A)

-   `target` = ブラウジング・コンテキストの名前、もしくは\_blank, \_self, \_parent, \_topのいずれか
    ハイパーリンクやフォームがナビゲーションを表している場合、base要素のtarget属性の値がデフォルト値になります。

## Examples

この例は関連ドキュメント<var>some-file.html</var>へのリンクを<var><http://example.org/deep/some-file.html></var>に書き換えています。

``` html
<!DOCTYPE html>
<html>
  <head>
    <title>base要素の例</title>
    <base href="http://www.example.org/deep/">
  </head>
  <body>
    <p><a href="some-file.html">関連リンク</a></p>
    <!-- 上記のリンクを解決すると下記のようになります -->
    <p><a href="http://www.example.org/deep/some-file.html">関連リンク</a></p>
  </body>
</html>
```

こちらの例では**base**要素より下に書かれている要素のみが影響を受けています。

``` html
<head>
  <title>base要素の例</title>
  <link href="my-style.css" rel="stylesheet">
  <base href="http://example.com">
  <link href="my-other-style.css" rel="stylesheet">
  <!--
    [current domain and directory]/my-style.css
    http://example.com/my-other-style.css
    のように解釈されます。
  -->
</head>
```

こちらの例では複数の**base**要素を記述していますが、無視されています。

``` html
<head>
  <title>base要素の例</title>
  <base href="http://example.com">
  <base target="_blank">
  <base href="http://webplatform.org" target="_top">
  <!--
    base要素の定義は1つにまとめられます：
    <base href="http://example.com/" target="_blank">
    例外として、Internet Explorerでは最初の要素のみが有効になります：
    <base href="http://example.com/" target="_self">
  -->
</head>
```

## Notes

-   Firefox 4とInternet Explorer 10は`<base>`要素に相対URLを指定することができます。これにより相対URLで相対URLを解釈することができます
    （訳注:その他のブラウザも対応しているようです）。
-   `<base>`はそれよりも下で記述した要素に対してのみ有効です。
-   複数の`<base>`を宣言するのは不正で、それぞれ最初の[`href`](/w/index.php?title=html/attributes/href/ja&action=edit&redlink=1)と[`target`](/w/index.php?title=html/attributes/target/ja&action=edit&redlink=1)のみが使用され、残りは破棄されます。Internet Explorer一番最初に書かれた`<base>`しか読んでくれません。

**注** インラインSVGで使われる`fill="url(#element-id)"`のような参照は`<base>`を使ったドキュメントでは問題になります。`url(#element-id)`で正しいURLが取得されますが、CSS セレクターでは正しく認識されません。 最新のFirefox とChrome ではその影響を非常に受けやすくなっています。

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/document-metadata.html#the-base-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-base-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/links.html#edef-BASE)
:   W3C Recommendation

## See also

### External resources

-   [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/HTML/Element/base)
-   [Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/ms535191%28v=vs.85%29.aspx)
