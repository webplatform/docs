---
title: 'area'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/imagemap.htm'
compatibility:
  feature: ja
  topic: html
lang: ja
notes:
  - 'Add more information in Summary, Notes and Compatibility sections.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLAreaElement](/dom/HTMLAreaElement)'
readiness: 'In Progress'
summary: イメージマップ上でハイパーリンクとして設定されるテキストとエリア、またはハイパーリンクとして設定しないエリアを表します。
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'html/global attributes/ja'
    - html/attributes/coords/ja
    - html/attributes/shape/ja
    - html/attributes/title/ja
    - html/attributes/alt/ja
    - html/attributes/href/ja
uri: html/elements/area/ja

---
## Summary

イメージマップ上でハイパーリンクとして設定されるテキストとエリア、またはハイパーリンクとして設定しないエリアを表します。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLAreaElement](/dom/HTMLAreaElement)

## HTML属性

 グローバル属性: accesskey, class, contenteditable, dir, hidden, id, lang, spellcheck, style, tabindex, title, translate
:   [グローバル属性](/w/index.php?title=html/global_attributes/ja&action=edit&redlink=1)を参照
 `alt` =イメージマップの代替テキスト
:   \<area\>要素でhref属性を指定していた場合、alt属性は必須です。
    同じイメージマップ（同一リソース）に対する別の\<area\>要素でalt属性に空白以外が指定されている場合、alt属性は空白のままにすることができます。
 `coords` = 有効な整数のリスト
:   この属性にはshape属性で記述した図形の座標を指定します。 この属性の処理はイメージマップの処理モデルの一部とされています。
    -   円の場合
        \<area\>要素のcoords属性に3つの整数を指定しなければいけません。この3つの内、最後の整数は負の値を指定できません。
        -   画像の左端から円の中心までのピクセル数
        -   画像の上端から円の中心までのピクセル数
        -   円の半径
    -   多角形の場合
        \<area\>要素のcoords属性に最低6つの、偶数個の整数を指定しなければいけません。整数のペアが画像の左上からの数えた座標となり、指定した順に多角形の角として扱われます。
    -   長方形の場合
        \<area\>要素のcoords属性に4つの整数を指定しなければいけません。1つ目の整数を3つ目より小さく、2つ目の整数を4つ目より小さく指定する必要があります。
        -   画像の左端から長方形の左側までののピクセル数
        -   画像の上端から長方形の上側までののピクセル数
        -   画像の左端から長方形の右側までののピクセル数
        -   画像の上端から長方形の下側までののピクセル数

`shape` = "circle" / "poly" / "rect" / "default"
:   -   `circle`: ハイパーリンクエリアが円の形になります。
    -   `poly`: ハイパーリンクエリアが長方形の形になります。
    -   `rect`: ハイパーリンクエリアが多角形の形になります。
    -   `default`: 画像全体がハイパーリンクとなります。coords属性を指定することはできません。

 `href` = URL（前後にスペースがある場合、取り除かれて扱われます。）
:   リンク先のURLを指定します。href属性を指定しない場合、プレースホルダーリンク（Javascript等で動的に生成したURLを設定するための空リンク）として扱われます。
 `target` = ブラウジング・コンテキストの名前またはキーワード
:   target = ブラウジング・コンテキストの名前またはキーワード
    ユーザエージェントがハイパーリンクを開くためのブラウジング・コンテキストの名前かキーワードを指定します。
    \<a\>要素のtarget属性はHTMLの過去のバージョンで非推奨となりましたが、iframe要素を組み込んでいるようなウェブアプリケーションでは未だに現役です。
    以下のいずれかの文字列を指定します。
    -   ブラウジング・コンテキストの名前
    -   大文字小文字問わず、以下の文字列と一致するもの： "\_blank", "\_self", "\_parent", "\_top"

 `rel` = スペース区切りのトークン
:   リンク元とリンク先の関係を表すトークンのリストを指定します。
 `hreflang` = 言語タグ
:   リンク先の言語を指定します。
    [BCP47]で定義されている言語タグのみ有効です。
 `media` = メディアクエリのリスト
:   リンク先をデザインするメディアを指定します。
    [MediaQueries]で定義されたメディアのみ有効です。
 `type` = MIMEタイプ
:   リンク先のMIMEタイプを指定します。
    [RFC2046]で定義された文字列のみ有効です。

## Examples

この例は親となる**\<map\>**要素の中で**\<area\>**要素を使い、太陽系のイメージマップを作成するHTMLです。各\<area\>要素が[**coords**](/w/index.php?title=html/attributes/coords/ja&action=edit&redlink=1)属性と[**shape**](/w/index.php?title=html/attributes/shape/ja&action=edit&redlink=1)属性を使ってmap要素の画像にハイパーリンクを設定しています。そして[**title**](/w/index.php?title=html/attributes/title/ja&action=edit&redlink=1)属性でマウスカーソルを当てた時にポップアップされるヒントを定義しています。このようなヒントは画像ファイルが存在しない、または何らかの理由で読み込むことができない場合などに有効です。

``` html
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
  "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
 <meta http-equiv="X-UA-Compatible" content="IE=8"/>
  <title>イメージマップの例</title>
  <base href="http://samples.msdn.microsoft.com"/>
</head>
<body>
<p><img src="/workshop/graphics/solarsys.png" width=504 height=126 border=0
    title="太陽系" usemap="#SystemMap"/></p>
  <map name="SystemMap">
      <area shape="rect" coords="0,0,82,126"
        href="/workshop/graphics/sun.png" title="太陽"/>
      <area shape="circle" coords="90,58,3"
        href="/workshop/graphics/merglobe.png" title="水星"/>
      <area shape="circle" coords="124,58,8"
        href="/workshop/graphics/venglobe.png" title="金星"/>
      <area shape="circle" coords="162,58,10"
        href="/workshop/graphics/earglobe.png" title="地球"/>
      <area shape="circle" coords="203,58,8"
        href="/workshop/graphics/marglobe.png" title="火星"/>
      <area shape="poly" coords="221,34,238,37,257,32,278,44,284,60,
        281,75,288,91,267,87,253,89,237,81,229,64,228,54"
        href="/workshop/graphics/jupglobe.png" title="木星"/>
      <area shape="poly" coords="288,19,316,39,330,37,348,47,351,66,
        349,74,367,105,337,85,324,85,307,77,303,60,307,50"
        href="/workshop/graphics/satglobe.png" title="土星"/>
      <area shape="poly" coords="405,39,408,50,411,57,410,71,404,78,
        393,80,383,86,381,75,376,69,376,56,380,48,393,44"
        href="/workshop/graphics/uraglobe.png" title="天王星"/>
      <area shape="poly" coords="445,38,434,49,431,53,427,62,430,72,
        435,77,445,92,456,77,463,72,463,62,462,53,455,47"
        href="/workshop/graphics/nepglobe.png" title="海王星"/>
      <area shape="circle" coords="479,66,3"
        href="/workshop/graphics/pluglobe.png" title="冥王星"/>
  </map>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/imagemap.htm)

## Notes

### 備考

-   \<area\>要素は1つの\<map\>要素に何個でも指定することができます。
-   [**coords**](/w/index.php?title=html/attributes/coords/ja&action=edit&redlink=1)属性のフォーマットは[**shape**](/w/index.php?title=html/attributes/shape/ja&action=edit&redlink=1)属性の値に依存します。
-   IE8以上（標準モード）において、\<img\>要素や\<map\>要素でヒントのポップアップを指定している場合、[**alt**](/w/index.php?title=html/attributes/alt/ja&action=edit&redlink=1)属性より[**title**](/w/index.php?title=html/attributes/title/ja&action=edit&redlink=1)属性を使うべきでしょう。また、[**href**](/w/index.php?title=html/attributes/href/ja&action=edit&redlink=1)属性の値はドキュメント互換モードに依存します。
-   この要素は画面上に描画されません。
-   この要素は終了タグ(\</area\>)が要りません。

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-area-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-area-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/objects.html#edef-AREA)
:   W3C Recommendation
