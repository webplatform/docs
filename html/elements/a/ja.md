---
title: ja
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Add more example'
summary: '<a>タグはハイパーリンクやリンク先を定義します。'
code_samples:
  - 'http://gist.github.com/5281100'
uri: html/elements/a/ja
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/attributes/href/ja
    - html/attributes/download/ja
    - html/attributes/id/ja
    - html/attributes/hreflang/ja
    - html/attributes/rel/ja
    - html/attributes/target/ja
    - html/attributes/name/ja
    - html/attributes/border/ja
    - html/attributes/tabIndex/ja
    - 'Template:Feature=a'

---
# a

## Summary

\<a\>タグはハイパーリンクやリンク先を定義します。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLAnchorElement](/dom/HTMLAnchorElement)

### 概要

`<a>`要素は外部サイトや、内部の別ページ・別セクション、画像やローカルファイルへのハイパーリンクを定義します。

### 構文

    <a href="[URI]">[アンカーテキストまたはイメージタグ]</a>

    <a id="#[ID]">[アンカーテキストまたはイメージタグ]</a>

    <a><a>[アンカーテキストまたはイメージタグ]</a></a>

### \<a\>\<a\>タグで囲まれたHTML

一般的にはテキストか画像を`<a></a>` タグで囲みます。 囲まれたHTMLはページ内に表示され、[href](/w/index.php?title=html/attributes/href/ja&action=edit&redlink=1)属性を指定していた場合はリンクとして描画されます。

### 一般的な属性

名前
:   値
[**download**](/w/index.php?title=html/attributes/download/ja&action=edit&redlink=1)
:   テキスト
[**href**](/w/index.php?title=html/attributes/href/ja&action=edit&redlink=1)
:   [URI](http://www.w3.org/Addressing/URL/uri-spec.html)
[**id**](/w/index.php?title=html/attributes/id/ja&action=edit&redlink=1)
:   識別用のテキスト
[**hreflang**](/w/index.php?title=html/attributes/hreflang/ja&action=edit&redlink=1)
:   [HTML5](http://www.ietf.org/rfc/bcp/bcp47.txt) または [HTML4](http://www.ietf.org/rfc/rfc1766.txt)用の言語タグ
[**rel**](/w/index.php?title=html/attributes/rel/ja&action=edit&redlink=1)
:   カンマ区切りのキーワードリスト
[**target**](/w/index.php?title=html/attributes/target/ja&action=edit&redlink=1)
:   [ブラウジング・コンテキスト](http://www.w3.org/TR/html5/browsers.html#valid-browsing-context-name-or-keyword)

## Examples

``` {.html}
<!-- 外部サイトへのリンク -->
<a href="http://www.example.com">ウェブサイト</a>

<!-- 同一ディレクトリの内部サイトへのリンク -->
<a href="home.html">ホーム</a>

<!-- ダウンロードリンク (HTML5のみ)。 download属性には保存ダイアログに予め設定するファイル名を指定します。
    download属性に値を設定しない場合、リソース名が設定されます。-->
<a href="filename_on_server.pdf" download="meaningful_filename.pdf">pdfファイルをダウンロード</a>

<!-- target属性で指定したウィンドウでリンクを開きます。 -->
<a href="http://www.example.com" target="_blank">新しいウィンドウでウェブサイトを開</a>

<!-- リンクの一部分としてimg要素を導入します -->
<a href="http://www.example.com"><img src="images/bullet.png">画像リンク</a>

<!-- ページ内のアンカーへのリンク -->
<a href="#top">トップへ</a>

<!-- アンカーを定義します。 -->
<a id="top"></a>

<!-- javascriptの関数を呼び出す (推奨されません) -->
<a href="javascript:alert('リンクがクリックされました')">リンクをクリックしてください</a>

<!-- ドキュメントへのリンクとリンク先のドキュメントとの関係をrel属性で指定します。 -->
<a href="http://www.example.com/help" rel="help">ヘルプへ</a>
```

[View live example](http://code.webplatform.org/gist/5281100)

## Notes

### 備考

ページ内にアンカーを作成する際、[**name**](/w/index.php?title=html/attributes/name/ja&action=edit&redlink=1) 属性はもはや誰も使っていません。[**id**](/w/index.php?title=html/attributes/id/ja&action=edit&redlink=1)で置き換えるべきでしょう。

テキストも画像もアンカーに指定することができます。アンカーとなった画像はフチに訪問済みかどうかを示す色がつくようになります。このフチの色を表示させないためには、"img"要素の[**border**](/w/index.php?title=html/attributes/border/ja&action=edit&redlink=1)属性に0を設定するか、**border**属性を省略する必要があります。CSS属性を使用することで、**a**要素と**img**要素のデフォルトの見た目を上書くことができます。

URIはhttpやmailto、fileなどのプロトコルを指定します。 フラグメント（\#に続くテキスト）を指定することで現在のページの特定の位置へジャンプできます。メニューの中の現在のページを参照するようなプレースホルダーリンクであることを示す場合、href属性は省略することができます

また、任意ですが、[**rel**](/w/index.php?title=html/attributes/rel/ja&action=edit&redlink=1)属性で対象のリンクにセマンティックな意味を付与することができます。

`a`要素に関連する国際化トピック：

-   [Indicating the language of a link destination](http://www.w3.org/International/techniques/authoring-html#linkdestination)

### クリックとフォーカス

ブラウザ/OS別　アンカーをクリックした際、自動でフォーカスが切り替わるか

アンカーをクリックしたときフォーカスされるか？

Desktop Browsers
:   Windows 8.1
Firefox 30.0
:   Yes
Chrome [\>=39](https://code.google.com/p/chromium/issues/detail?id=388666)
:   Yes
Safari 7.0.5
:   N/A
Internet Explorer 11
:   Yes
Presto (Opera 12)
:   Yes

アンカーをタップしたときフォーカスされるか？

Mobile Browsers
:   iOS 7.1.2
Safari Mobile
:   [`tabindex`](/w/index.php?title=html/attributes/tabIndex/ja&action=edit&redlink=1)のみ
Chrome 35
:   ???

�

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-a-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-a-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/links.html#edef-A)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/a)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

[Template:Feature=a](/w/index.php?title=Template:Feature%3Da&action=edit&redlink=1)

