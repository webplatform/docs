---
title: 'a'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/a)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5281100'
compatibility:
  feature: ja
  topic: html
lang: ja
notes:
  - 'Add more example'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLAnchorElement](/dom/HTMLAnchorElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: '&lt;a&gt;タグはハイパーリンクやリンク先を定義します。'
tags:
  - Markup
  - Elements
  - HTML
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
uri: html/elements/a/ja

---
<p>
</p>
<h2>Summary</h2>
<p>
&amp;lt;a&amp;gt;タグはハイパーリンクやリンク先を定義します。</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLAnchorElement">HTMLAnchorElement</a></dd>
</dl><h3>概要</h3>
<p><code>&lt;a&gt;</code>要素は外部サイトや、内部の別ページ・別セクション、画像やローカルファイルへのハイパーリンクを定義します。
</p>
<h3>構文</h3>
<pre>&lt;a href="[URI]"&gt;[アンカーテキストまたはイメージタグ]&lt;/a&gt;</pre>
<pre>&lt;a id="#[ID]"&gt;[アンカーテキストまたはイメージタグ]&lt;/a&gt;</pre>
<pre>&lt;a&gt;&lt;a&gt;[アンカーテキストまたはイメージタグ]&lt;/a&gt;&lt;/a&gt;</pre>
<h3>&lt;a&gt;&lt;a&gt;タグで囲まれたHTML</h3>
<p>一般的にはテキストか画像を<code>&lt;a&gt;&lt;/a&gt;</code> タグで囲みます。
囲まれたHTMLはページ内に表示され、<a href="/w/index.php?title=html/attributes/href/ja&amp;action=edit&amp;redlink=1" class="new">href</a>属性を指定していた場合はリンクとして描画されます。
</p><p><br/></p>
<h3>一般的な属性</h3>
<table class="wikitable"><tr><th> 名前
</th>
<th> 値
</th>
<th> 目的
</th>
<th> 例
</th>
<th> 有効
</th></tr><tr><td> <a href="/w/index.php?title=html/attributes/download/ja&amp;action=edit&amp;redlink=1" class="new"><b>download</b></a>
</td>
<td> テキスト
</td>
<td> 保存ダイアログに表示するファイル名を指定することができます
</td>
<td> <pre>download="filename.pdf"</pre>
</td>
<td> HTML5
</td></tr><tr><td> <a href="/w/index.php?title=html/attributes/href/ja&amp;action=edit&amp;redlink=1" class="new"><b>href</b></a>
</td>
<td> <a rel="nofollow" class="external text" href="http://www.w3.org/Addressing/URL/uri-spec.html">URI</a>
</td>
<td> 対象のリンクを指定します
</td>
<td> <pre>href="http://example.com"</pre> <pre>href="#TableOfContents"</pre>
</td>
<td>  
</td></tr><tr><td> <a href="/w/index.php?title=html/attributes/id/ja&amp;action=edit&amp;redlink=1" class="new"><b>id</b></a>
</td>
<td> 識別用のテキスト
</td>
<td> hrefで参照するためのアンカーを生成します
</td>
<td> <pre>id="TableOfContents"</pre>
</td>
<td>  
</td></tr><tr><td> <a href="/w/index.php?title=html/attributes/hreflang/ja&amp;action=edit&amp;redlink=1" class="new"><b>hreflang</b></a>
</td>
<td> <a rel="nofollow" class="external text" href="http://www.ietf.org/rfc/bcp/bcp47.txt">HTML5</a> または <a rel="nofollow" class="external text" href="http://www.ietf.org/rfc/rfc1766.txt">HTML4</a>用の言語タグ
</td>
<td> リンク先の言語のヒントです。 リンク元からリンク先へのヒントとしてrel="alternate"とともに記述して使用できます。
</td>
<td> <pre>hreflang="ja"</pre>
</td></tr><tr><td> <a href="/w/index.php?title=html/attributes/rel/ja&amp;action=edit&amp;redlink=1" class="new"><b>rel</b></a>
</td>
<td> カンマ区切りのキーワードリスト
</td>
<td> 現在のページとリンク先の関係を示します
</td>
<td> <pre>rel="help"</pre>
</td>
<td>  
</td></tr><tr><td> <a href="/w/index.php?title=html/attributes/target/ja&amp;action=edit&amp;redlink=1" class="new"><b>target</b></a>
</td>
<td> <a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/browsers.html#valid-browsing-context-name-or-keyword">ブラウジング・コンテキスト</a>
</td>
<td> リンクをどこで開くか指定できます
</td>
<td> <pre>target="_blank"</pre>
</td>
<td>  
</td></tr></table><h2>Examples</h2>
<div class="example">
<pre class="html">
&lt;!-- 外部サイトへのリンク --&gt;
&lt;a href="http://www.example.com"&gt;ウェブサイト&lt;/a&gt;

&lt;!-- 同一ディレクトリの内部サイトへのリンク --&gt;
&lt;a href="home.html"&gt;ホーム&lt;/a&gt;

&lt;!-- ダウンロードリンク (HTML5のみ)。 download属性には保存ダイアログに予め設定するファイル名を指定します。
    download属性に値を設定しない場合、リソース名が設定されます。--&gt;
&lt;a href="filename_on_server.pdf" download="meaningful_filename.pdf"&gt;pdfファイルをダウンロード&lt;/a&gt;

&lt;!-- target属性で指定したウィンドウでリンクを開きます。 --&gt;
&lt;a href="http://www.example.com" target="_blank"&gt;新しいウィンドウでウェブサイトを開&lt;/a&gt;

&lt;!-- リンクの一部分としてimg要素を導入します --&gt;
&lt;a href="http://www.example.com"&gt;&lt;img src="images/bullet.png"&gt;画像リンク&lt;/a&gt;

&lt;!-- ページ内のアンカーへのリンク --&gt;
&lt;a href="#top"&gt;トップへ&lt;/a&gt;

&lt;!-- アンカーを定義します。 --&gt;
&lt;a id="top"&gt;&lt;/a&gt;

&lt;!-- javascriptの関数を呼び出す (推奨されません) --&gt;
&lt;a href="javascript:alert('リンクがクリックされました')"&gt;リンクをクリックしてください&lt;/a&gt;

&lt;!-- ドキュメントへのリンクとリンク先のドキュメントとの関係をrel属性で指定します。 --&gt;
&lt;a href="http://www.example.com/help" rel="help"&gt;ヘルプへ&lt;/a&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/5281100">View live example</a>
</p>
</div>
<h2>Notes</h2>
<h3>備考</h3>
<p>ページ内にアンカーを作成する際、<a href="/w/index.php?title=html/attributes/name/ja&amp;action=edit&amp;redlink=1" class="new"><b>name</b></a> 属性はもはや誰も使っていません。<a href="/w/index.php?title=html/attributes/id/ja&amp;action=edit&amp;redlink=1" class="new"><b>id</b></a>で置き換えるべきでしょう。
</p><p>テキストも画像もアンカーに指定することができます。アンカーとなった画像はフチに訪問済みかどうかを示す色がつくようになります。このフチの色を表示させないためには、"img"要素の<a href="/w/index.php?title=html/attributes/border/ja&amp;action=edit&amp;redlink=1" class="new"><b>border</b></a>属性に0を設定するか、<b>border</b>属性を省略する必要があります。CSS属性を使用することで、<b>a</b>要素と<b>img</b>要素のデフォルトの見た目を上書くことができます。
</p><p>URIはhttpやmailto、fileなどのプロトコルを指定します。
フラグメント（#に続くテキスト）を指定することで現在のページの特定の位置へジャンプできます。メニューの中の現在のページを参照するようなプレースホルダーリンクであることを示す場合、href属性は省略することができます
</p><p>また、任意ですが、<a href="/w/index.php?title=html/attributes/rel/ja&amp;action=edit&amp;redlink=1" class="new"><b>rel</b></a>属性で対象のリンクにセマンティックな意味を付与することができます。
</p><p><code>a</code>要素に関連する国際化トピック：
</p>
<ul><li> <a rel="nofollow" class="external text" href="http://www.w3.org/International/techniques/authoring-html#linkdestination">Indicating the language of a link destination</a></li></ul><h3>クリックとフォーカス</h3>
<p>ブラウザ/OS別　アンカーをクリックした際、自動でフォーカスが切り替わるか
</p><p>アンカーをクリックしたときフォーカスされるか？
</p>
<table class="wikitable"><tr><th>Desktop Browsers
</th>
<td>Windows 8.1
</td>
<td>OS X 10.9
</td></tr><tr><th>Firefox 30.0
</th>
<td>Yes
</td>
<td>Yes
</td></tr><tr><th>Chrome <a rel="nofollow" class="external text" href="https://code.google.com/p/chromium/issues/detail?id=388666">&gt;=39</a>
</th>
<td>Yes
</td>
<td>Yes
</td></tr><tr><th>Safari 7.0.5
</th>
<td>N/A
</td>
<td><a href="/w/index.php?title=html/attributes/tabIndex/ja&amp;action=edit&amp;redlink=1" class="new"><code>tabindex</code></a>のみ
</td></tr><tr><th>Internet Explorer 11
</th>
<td>Yes
</td>
<td>N/A
</td></tr><tr><th>Presto (Opera 12)
</th>
<td>Yes
</td>
<td>???
</td></tr></table><p>アンカーをタップしたときフォーカスされるか？
</p>
<table class="wikitable"><tr><th>Mobile Browsers
</th>
<td>iOS 7.1.2
</td>
<td>Android 4.4.4
</td></tr><tr><th>Safari Mobile
</th>
<td><a href="/w/index.php?title=html/attributes/tabIndex/ja&amp;action=edit&amp;redlink=1" class="new"><code>tabindex</code></a>のみ
</td>
<td>N/A
</td></tr><tr><th>Chrome 35
</th>
<td>???
</td>
<td><a href="/w/index.php?title=html/attributes/tabIndex/ja&amp;action=edit&amp;redlink=1" class="new"><code>tabindex</code></a>のみ
</td></tr></table><p> 
</p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html51/text-level-semantics.html#the-a-element">HTML 5.1</a></dt>
  <dd>W3C Working Draft</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/text-level-semantics.html#the-a-element">HTML 5</a></dt>
  <dd>W3C Recommendation</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html401/struct/links.html#edef-A">HTML 4.01</a></dt>
  <dd>W3C Recommendation</dd>
</dl><p><a href="/w/index.php?title=Template:Feature%3Da&amp;action=edit&amp;redlink=1" class="new">Template:Feature=a</a>
</p><p><br/></p>
