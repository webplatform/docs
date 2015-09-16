---
title: body
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://test.w3.org/html/examples/elements/body/body01.html'
lang: ja
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLBodyElement](/dom/HTMLBodyElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'body要素はドキュメントの主要コンテンツを表します。'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/body/ja

---
## Summary

body要素はドキュメントの主要コンテンツを表します。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLBodyElement](/dom/HTMLBodyElement)

`<body>`要素はスクリプトからアクセスすることができます。

\<body\>要素を持つウィンドウオブジェクトは`onblur`、`onfocus`、`onload`、`onunload`イベントをハンドリングすることができます。

### HTMLイベントハンドラコンテンツ属性

|Event|Description|
|:----|:----------|
|`onafterprint`|ユーザが現在のドキュメントを印刷|
|`onbeforeprint`|ユーザが現在のドキュメントの印刷をリクエスト|
|`onbeforeunload`|ドキュメントがunloadされようとしている|
|`onblur`|ドキュメントからフォーカスが外れた|
|`onerror`|ドキュメントがプロパティの読み込みに失敗|
|`onfocus`|ドキュメントがフォーカスされた|
|`onhashchange`|ドキュメントの現在のアドレスのフラグメント識別子が変更された|
|`onload`|ドキュメントのロードが完了|
|`onmessage`|ドキュメントがメッセージを受信|
|`onoffline`|ネットワークのコネクションが失敗|
|`ononline`|ネットワークのコネクションが復帰|
|`onpopstate`|ユーザがセッションヒストリーを遷移|
|`onredo`|ユーザがトランザクション履歴をやり直した|
|`onresize`|ドキュメントのビューがリサイズされた|
|`onstorage`|ドキュメントのビューがリサイズされた|
|`onundo`|ユーザがトランザクション履歴を取り消した|
|`onunload`|現在のドキュメントから移動|

以下の属性は、もう使われておらず、今後は使うべきではありません。

`alink`, `bgcolor`, `link`, `marginbottom`, `marginheight`, `marginleft`, `marginright`, `margintop`, `marginwidth`, `text`, `vlink`.

## Examples

`<body>`要素が`<head>`に続き、全体が`<html>`要素に含まれています。

``` html


<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>The HTML Document</title>
</head>
<body>
<p>The HTML content</p>
</body>
</html>
```

</pre>
[View live example](http://test.w3.org/html/examples/elements/body/body01.html)

この例では、javascriptで`<body>`を取得します。

``` js


var oBody = document.body;
```

</pre>

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-body-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/sections.html#the-body-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-BODY)
:   W3C Recommendation
