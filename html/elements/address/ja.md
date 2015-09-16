---
title: 'address'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: ja
  topic: html
lang: ja
notes:
  - 'Add syntax, attribute, example, compatibility.'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Not Ready'
summary: '&lt;address&gt;は文書や記事の所有者・著者とコンタクトをとるための情報を囲む要素です。'
tags:
  - Markup
  - Elements
  - HTML
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
uri: html/elements/address/ja

---
<p><br/></p>
<h2>Summary</h2>
<p>
&amp;lt;address&amp;gt;は文書や記事の所有者・著者とコンタクトをとるための情報を囲む要素です。</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLElement">HTMLElement</a></dd>
</dl><ul><li> &lt;address&gt;要素は、addressと言っても住所情報を記載するためものではありません。（実際に関連する住所情報の場合は別ですが）</li>
<li> &lt;address&gt;には連絡を取るための情報以外の情報を記載してはいけません。</li>
<li> 一般的に、&lt;address&gt;要素は&lt;footer&gt;要素の中で、他の情報の間に記載します。</li></ul><h2>Examples</h2>
<p>W3Cのサイトでは以下の様な連絡先情報を記載しています。
</p>
<div class="example">
<pre class="html">
&lt;address&gt;
    &lt;p&gt;&lt;a href="http://www.w3.org/Consortium/contact-mit"&gt;MIT&lt;/a&gt;&lt;/p&gt;
&lt;/address&gt;

</pre>
<p><br/></p>
</div>
<p>&lt;address&gt;要素の中に以下のような情報（最終更新日時など）を入れるのは正しくありません。
</p>
<div class="example">
<pre class="html">
&lt;div&gt;Last Modified: 1999/12/24 23:37:50&lt;/div&gt;

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<p>WebKit（safariや古いAndroid系）やTrident（Internet Explorer）では以下のようにデフォルトでスタイルが設定されています。
</p>
<pre>address {
	display:block;
	font-style: italic;
}</pre>
<p>Gecko(Firefox)では以下のように設定されています。
</p>
<pre>address, address[dir]{
         unicode-bidi: -moz-isolate;
         display:block;
         font-style:italic;
}</pre>
<h3>標準情報</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=25320">HTML 4.01 Specification</a>, Section 7.5.6</li></ul><p><br/></p>
<h3>HTML情報</h3>
<table class="wikitable"><tr><th>Closing Tag
</th>
<td>required
</td></tr><tr><th>CSS Display
</th>
<td>block
</td></tr></table><p> 
</p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html51/sections.html#the-address-element">HTML 5.1</a></dt>
  <dd>W3C Working Draft</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/sections.html#the-address-element">HTML 5</a></dt>
  <dd>W3C Recommendation</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html401/struct/global.html#edef-ADDRESS">HTML 4.01</a></dt>
  <dd>W3C Recommendation</dd>
</dl>
