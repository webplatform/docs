---
title: 'Web標準モデル HTMLとCSS、JavaScript'
lang: ja
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
summary: "concepts/internet_and_web/How_does_the_Internet_Workの続きです。 HTMLと CSS、JavaScript\nが取り入れられました。それではもう少し掘り下げて、この3つがwebサイトを作る際に何をしてどのように連携するのか、それぞれを見ていくことにしましょう。\n"
tags:
  - Concept_Pages
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'concepts/Internet and Web/The Web Standards Model/af'
    - 'concepts/Internet and Web/The Web Standards Model/ar'
    - 'concepts/Internet and Web/The Web Standards Model/ast'
    - 'concepts/Internet and Web/The Web Standards Model/az'
    - 'concepts/Internet and Web/The Web Standards Model/bcc'
    - 'concepts/Internet and Web/The Web Standards Model/bg'
    - 'concepts/Internet and Web/The Web Standards Model/br'
    - 'concepts/Internet and Web/The Web Standards Model/ca'
    - 'concepts/Internet and Web/The Web Standards Model/cs'
    - 'concepts/Internet and Web/The Web Standards Model/da'
    - 'concepts/Internet and Web/The Web Standards Model/de'
    - 'concepts/Internet and Web/The Web Standards Model/diq'
    - 'concepts/Internet and Web/The Web Standards Model/el'
    - 'concepts/Internet and Web/The Web Standards Model/eo'
    - 'concepts/Internet and Web/The Web Standards Model/es'
    - 'concepts/Internet and Web/The Web Standards Model/fa'
    - 'concepts/Internet and Web/The Web Standards Model/fi'
    - 'concepts/Internet and Web/The Web Standards Model/fr'
    - 'concepts/Internet and Web/The Web Standards Model/gl'
    - 'concepts/Internet and Web/The Web Standards Model/gu'
    - 'concepts/Internet and Web/The Web Standards Model/he'
    - 'concepts/Internet and Web/The Web Standards Model/hu'
    - 'concepts/Internet and Web/The Web Standards Model/hy'
    - 'concepts/Internet and Web/The Web Standards Model/id'
    - 'concepts/Internet and Web/The Web Standards Model/it'
    - 'concepts/Internet and Web/The Web Standards Model/ka'
    - 'concepts/Internet and Web/The Web Standards Model/kk'
    - 'concepts/Internet and Web/The Web Standards Model/km'
    - 'concepts/Internet and Web/The Web Standards Model/ko'
    - 'concepts/Internet and Web/The Web Standards Model/ksh'
    - 'concepts/Internet and Web/The Web Standards Model/kw'
    - 'concepts/Internet and Web/The Web Standards Model/mk'
    - 'concepts/Internet and Web/The Web Standards Model/ml'
    - 'concepts/Internet and Web/The Web Standards Model/mr'
    - 'concepts/Internet and Web/The Web Standards Model/ms'
    - 'concepts/Internet and Web/The Web Standards Model/nl'
    - 'concepts/Internet and Web/The Web Standards Model/no'
    - 'concepts/Internet and Web/The Web Standards Model/oc'
    - 'concepts/Internet and Web/The Web Standards Model/pl'
    - 'concepts/Internet and Web/The Web Standards Model/pt'
    - 'concepts/Internet and Web/The Web Standards Model/pt-br'
    - 'concepts/Internet and Web/The Web Standards Model/ro'
    - 'concepts/Internet and Web/The Web Standards Model/ru'
    - 'concepts/Internet and Web/The Web Standards Model/si'
    - 'concepts/Internet and Web/The Web Standards Model/sk'
    - 'concepts/Internet and Web/The Web Standards Model/sl'
    - 'concepts/Internet and Web/The Web Standards Model/sq'
    - 'concepts/Internet and Web/The Web Standards Model/sr'
    - 'concepts/Internet and Web/The Web Standards Model/sv'
    - 'concepts/Internet and Web/The Web Standards Model/ta'
    - 'concepts/Internet and Web/The Web Standards Model/th'
    - 'concepts/Internet and Web/The Web Standards Model/tr'
    - 'concepts/Internet and Web/The Web Standards Model/uk'
    - 'concepts/Internet and Web/The Web Standards Model/vi'
    - 'concepts/Internet and Web/The Web Standards Model/yue'
    - 'concepts/Internet and Web/The Web Standards Model/zh'
    - 'concepts/Internet and Web/The Web Standards Model/zh-hans'
    - 'concepts/Internet and Web/The Web Standards Model/zh-hant'
    - 'concepts/Internet and Web/The Web Standards Model/zh-tw'
uri: 'concepts/Internet and Web/The Web Standards Model/ja'

---
<h2>Summary</h2>
<p>
concepts/internet_and_web/How_does_the_Internet_Workの続きです。 HTMLと CSS、JavaScript
が取り入れられました。それではもう少し掘り下げて、この3つがwebサイトを作る際に何をしてどのように連携するのか、それぞれを見ていくことにしましょう。
</p><p><br/></p>
<h2>分けた理由は?</h2>
<p>web標準について質問されるもので、一番多いのがこれです。HTMLを使ってデザインとレイアウトをし、コンテンツを完成できます。フォント・エレメントはスタイルに使い、HTMLのテーブルはレイアウトに使いますが、どうしてXHTMLやCSSで悩む必要があるのでしょうか? レイアウトに使うテーブルなどは、webデザインがまだまだな過去において使われていましたが、いまだに使う人が大勢います(皆さんはそうしないで)。そもそもこのコースを作った理由の一つがこのためです。そのような方法はこのコースでは扱いません。ここでは旧式の方法に対して、CSSとHTMLを使う理由として、納得できるものをあげます。
</p>
<ol><li> 「効率的なコード」: ファイルが大きく長くなればなるほど、ダウンロードに時間がかかります。そうすると、見るのに時間がかかる人がいます(ダウンロードするのにメガバイト単位で課金される人もいます)。なので、HTMLファイル毎にデザインやレイアウトの情報をまき散らした大きなページで帯域を浪費したくないと考えるでしょう。HTMLファイルを必要最低限に整理し、デザインとレイアウトを独立した1つのCSSファイルとして、1回だけ取り込みましょう。このケースの実例をみるなら、<a rel="nofollow" class="external text" href="http://www.alistapart.com/articles/slashdot/">the A List Apart Slashdot rewrite article</a>です。ここでは、作者が著名なサイトをとりあげ、XHTMLとCSSで書き直しをしています。</li>
<li> 「メンテナンスが容易」: 引き続きになりますが、デザインとレイアウト情報を1か所にだけ指定しておけば、サイトのページの見た目を変更したい時に、1か所だけ更新すればよくなります。サイトのページ毎に情報を更新する方がよいですか? 私はそうは思いません。</li>
<li> 「アクセシビリティ」: 視覚に障害があるWebユーザは、「スクリーン・リーダー」というソフトウェアが使えます。これを使って、見た目ではなく音で情報にアクセスします。文字通り、ページを読んでユーザーへ伝えます。さらによいことには、そのページが見出しやパラグラフといったしっかりした意味構造を持っていれば、webページを案内することもできます。加えて、最良の方法で構築してあれば、webページでキーボードをコントロールすることさえできます(マウスが使えない運動障害をもった人にとって重要です)。</li></ol><p>最後に、スクリーン・リーダーは、画像に組み込まれたテキストにはアクセスできず、JavaScriptを使ったものでも間違えてしまうことがあります。大事なコンテンツは誰にでも利用できるようにする、ということが大切です。
</p>
<ol><li> 「デバイス・コンパチビリティ」: HTMLやXHTMLが、デザインする情報がないシンプルなマークアップなら、ばらばらな属性(例えば、スクリーンサイズ)をもったデバイスたちでも、代わりとなるスタイルシートを適用するだけで再フォーマットできます。こうするのに方法はいくつかあります(この点については ([<a rel="nofollow" class="external text" href="http://dev.opera.com/articles/mobile/">mobile articles on dev.opera.com</a>] を参照してください)。CSSにも様々な体裁を整えるメソッドと、メディアタイプのためにスタイルシートを指定できるようになっています(例えば、スクリーンで見る、印刷する、モバイルデバイスで見る)。</li>
<li> 「Webクローラと検索エンジン」: 多分 Googleや他の検索エンジンが見つけやすいページを望んでいるのではないでしょうか。検索エンジンは「クローラ」という特殊なソフトウェアでページを読み回っています。クローラがページのコンテンツを見つけるのに支障が出たり、見出しを見出しとして定義していない等してしまい、何が重要なのかの判断を間違えてしまうと、恐らく適切な検索結果のランキングがおかしなことになってしまうでしょう。</li>
<li> 「よいものはよい」:  「俺が言ったんだから」的な理由ぽいです。しかし、プロで標準にあかるい開発者やデザイナーと話すと、コンテンツとデザイン、動作を分けることはwebアプリケーションの開発にとってベストだと言うでしょう。</li></ol><h2>マークアップ、ページの基本</h2>
<p>HTMLとXHTMLはマークアップ言語で、属性(オプションのものも必須のものもあります)をともなったエレメントで構成されています。エレメントは、ドキュメントの様々なタイプのコンテンツをマークアップするのに利用され、webブラウザでどの小さなコンテンツがレンダリングされるのかを指定します(例えば、見出しやパラグラフ、テーブル、箇条書き等)。
</p><p>エレメントは、実際にコンテンツタイプを定義します。一方属性はエレメントについての追加情報を定義します。IDのようにエレメントを特定するものや、リンクがどこを指すのかを示す locationがあります。
マークアップはできるだけ意味を持たせるように心がけてください。つまり、コンテンツの機能を一意に表現するようにします。Figure 1 は代表的なエレメントの構造です。
</p><p>
<img alt="&#x4EE3;&#x8868;&#x7684;&#x306A;HTML&#x30A8;&#x30EC;&#x30E1;&#x30F3;&#x30C8;" src="/assets/public/6/62/article4-1.gif" width="600" height="191"/></p><p>Figure 1: (X)HTML の構造
</p><p>その点を考慮すると、HTMLとXHTMLの違いはどこにあるのでしょうか?
</p>
<h3>XHTMLとは?</h3>
<p>HTMLはもっとも古いweb言語で、webで見られる一番ありきたりなものです。厳しいシンタックスのルールと比べると、多少はルールが緩くなっています。それとは対照的に、XHTMLはXMLの語彙をもってHTMLを改善したものです。XMLは独自のマークアップ言語で、シンタックスのルールが厳しくなっています。XHTMLとHTMLの違いは、実際それほど大きいものではありません。あなたが将来、どこか癖のあるスタイルを持ったコーディング・ガイドラインを持ったどこかのwebチームで活動することになる場合を除けば。もしHTML5を使うのなら(このコースではそうしていきますが)、HTMLやXHTMLのシンタックスが使えます。
</p><p>HTMLとXHTMLのシンタックス上の主な違い。
(引用元: <a rel="nofollow" class="external text" href="http://www.w3.org/community/webed/wiki/The_web_standards_model_-_HTML_CSS_and_JavaScript">The web standards model</a>)
</p><p>HTML:
</p>
<ul><li> エレメントと属性は、大文字・小文字の区別がありません。例えば、<code>&lt;h1&gt;</code> と <code>&lt;H1&gt;</code> は同じです。</li>
<li> 閉じタグを必要としないエレメントがあります(例えば、paragraphs や <code>&lt;p&gt;</code>))。一方でその他(「空要素」という)は、閉じタグがありません(例えば、画像の <code>&lt;img&gt;</code>)。</li>
<li> 属性値は、引用符で囲まなくても書ける場合があります。</li>
<li> ショートハンドが使える属性があります(つまり、<code>&lt;input required&gt;</code>)</li></ul><p>XHTML:
</p>
<ul><li> エレメントと属性は、大文字・小文字の区別があります。全て小文字です。</li>
<li> エレメントはすべて、明示的に閉じなければいけません(例えば、<code>&lt;p&gt;A paragraph&lt;/p&gt;</code>)。コンテンツがないエレメントは、開始タグ中でスラッシュを使って閉じなければいけません(例えば、<code>&lt;hr&gt;&lt;/hr&gt;</code> と</li></ul><pre><code>&lt;hr/&gt;</code> は同じ意味です)。
</pre>
<ul><li> 属性は、引用符で囲まなければいけません。</li>
<li> 全ての属性は、省略しない形式を使わなければいけません(<code>&lt;input required="required"&gt;</code>)。</li></ul><p><br/>
Table 1: HTML と XHTML の違い
</p>
<h3>検証とは?</h3>
<p>HTMLとXHTMLは標準なので(さらに言えば、CSSも)、the World Wide Web Consortium (W3C)はページを自動的にチェックするバリデーターという素晴らしいツールを作りました。このツールは、閉じタグ忘れや属性の引用符忘れといった、コードにある問題やエラーを指摘します。 <a rel="nofollow" class="external text" href="http://validator.w3.org/">The HTML validator is available online</a>は、HTMLかXHTMLどちらを使っているのか、どのドキュメントタイプを使っているのかを自動的に判定します。CSSをチェックしたいなら、<a rel="nofollow" class="external text" href="http://jigsaw.w3.org/css-validator/">CSS validator を利用できます</a> <a rel="nofollow" class="external text" href="http://html5.validator.nu/">HTML5 validator</a> というものもあり、W3CのものよりもHTML5関連については進んでいます。
</p><p>検証についてさらに知りたいなら、<a rel="nofollow" class="external text" href="http://www.w3.org/wiki/Validating_your_HTML">Validating your HTML</a> を見てください。ドキュメントタイプについてさらに知りたいなら、<a rel="nofollow" class="external text" href="http://www.w3.org/wiki/Choosing_the_right_doctype_for_your_HTML_documents">Choosing the right doctype for your HTML documents</a> を見てください。
</p>
<h2>CSS — スタイルを追加する</h2>
<p>カスケーディング・スタイル・シートを使うと、ドキュメントの整形やレイアウトをうまくコントロールできます。体系的な規則にもとづいて処理を行い、スタイルしたいエレメントを選んで、エレメントの様々なプロパティに値を設定します。色や背景、フォントサイズ、スタイルを変更したり、追加したりできます。別の場所にあるwebページに設定することさえできます。これはCSSのルールの例です。
</p><p><br/></p>
<pre class="css">
p {
   line-height: 2;
   color: green;
}

</pre>
<p><br/><code>&lt;p&gt;&lt;/p&gt;</code> タグ内に囲まれたコンテンツは、2倍の行間でグリーンになります。
</p><p>下記の例は、CSSがHTMLをどのようにデザインするのかについてヒントをくれるでしょう。さらにCSSを知りたいなら <a rel="nofollow" class="external text" href="http://www.w3.org/wiki/CSS_basics">CSS basics</a> から始めましょう。
</p>
<h2>JavaScript — webページに動きを加える</h2>
<p>最後になりますが、JavaScriptはwebページに動きをもたらすのに使うスクリプト言語です。フォームに入力したデータを検証したり(入力が正しいフォーマットかどうか、問い合わせる)、ドラッグ＆ドロップを実装したり、その場でスタイルを変更したり、メニューのようなエレメントを動かしたり、ボタンの機能を操作したりと、他にも山ほどの機能を用意しています。最近のJavaScriptは、ターゲットとなるHTMLの要素を見つけ出し、それに対して何かを働きかけます。まさにCSSと同じですが、操作もシンタックスも随分と違います。
</p><p>JavaScriptは、HTMLやCSSと比べて複雑で範囲が広い課題です。なので、この段階で混乱を避けるために、シンプルなままにしておきます。このコースでは <a rel="nofollow" class="external text" href="http://www.w3.org/wiki/Programming_-_the_real_basics">Programming - the real basics</a> まで、JavaScriptは登場しません。
</p>
<h2>例のページ</h2>
<p>カバーしてこなかった詳細なことは、たくさんあります。しかし、このwebデザインコースを通じて、全てを見ていきましょう! ここで実際のページ例をお見せして、この文書の残りで皆さんがすることになる雰囲気を感じ取ってください。
</p><p>下記にあげた例は文献ページです。web開発チームにおける集団力学についての心理学のエッセーや米国におけるブロードバンド・インターネットの利用についての取り組みのレポートといった、主張したいことの最後に文献を引用するのに使えます。厳しい学術的なライティングにこだわるなら、この例はAPA形式(私はそれを取り上げざる得ない)で表現します。 <a rel="nofollow" class="external text" href="http://dev.opera.com/articles/view/4-the-web-standards-model-html-css-a/article4_examples.zip">この例のHTMLとCSSが入ったzipファイルがダウンロードできます。</a>
</p>
<h3>index.html</h3>
<pre class="html">
&lt;!DOCTYPE html&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
  &lt;meta charset="utf-8"/&gt;
  &lt;title&gt;References&lt;/title&gt;
  &lt;style type="text/css"&gt;
    @import url("styles.css");
  &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;div id="bggraphic"&gt;&lt;/div&gt;
  &lt;div id="header"&gt;
    &lt;h1&gt;References&lt;/h1&gt;
  &lt;/div&gt;
  &lt;div id="references"&gt;
    &lt;cite class="article"&gt;Adams, J. R. (2008). The Benefits of Valid Markup: A Post-Modernistic
    Approach to Developing
    Websites. &lt;em&gt;The Journal of Awesome Web Standards, 15:7,&lt;/em&gt; 57-62.&lt;/cite&gt;
    &lt;cite class="book"&gt;Baker, S. (2006). &lt;em&gt;Validate Your Pages.... Or Else!.&lt;/em&gt;
    Detroit, MI: Are you out of your mind publishers.&lt;/cite&gt;
    &lt;cite class="article"&gt;Lane, J. C. (2007). Dude, HTML 4, that's like so 2000. &lt;em&gt;The
     Journal that Publishes Genius, 1:2, &lt;/em&gt; 12-34.&lt;/cite&gt;
    &lt;cite class="website"&gt;Smith, J. Q. (2005). &lt;em&gt;Web Standards and You.&lt;/em&gt;
    Retrieved May 3, 2007 from Web standards and you.&lt;/cite&gt;
  &lt;/div&gt;
  &lt;div id="footer"&gt;
    &lt;p&gt;The content of this page is copyright © 2007 &lt;a href="mailto:jonathan.lane@gmail.com"&gt;J. Lane&lt;/a&gt;&lt;/p&gt;
  &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;

</pre>
<p><br/>
このファイルを一行一行分析するつもりはありません。それは、これからいくつもの例を見ていくことになるからです。
しかしながら、代表的なものを次に取り上げます。
</p><p>1行目は、ドキュメントタイプ宣言かドキュメントタイプというものです。この場合は、HTML5のページとなります。ドキュメントタイプのそもそもの考え方は、マークアップ言語に対して、守らなければならないルールを適用するというものでした。検証されても問題なく、実際全て満たしていれば、ブラウザは正確に「標準モード」でレンダリングできます。HTML5のドキュメントタイプは、この機能を実現するのに最も短い文字列です。ドキュメントタイプについてさらに詳しく知りたいなら、 <a rel="nofollow" class="external text" href="http://www.w3.org/wiki/Choosing_the_right_doctype_for_your_HTML_documents">Choosing the right doctype for your HTML documents</a>  をご覧ください。
</p><p>5~7行目では、CSSファイルをページにインポートしています。このファイルに含まれたスタイルが、ページにある色々なエレメントへと適用されます。次のセクションでは、ページのフォーマットすべてを操作するCSSファイルの中身を見ることにします。異なる文献それぞれに別のクラスを割り当ててあります。こうすることで、文献のそれぞれのタイプに違うスタイルを適用できます。例えば、リストを検索しやすくするために、それぞれの文献の右側に違う色を付けました。
</p><p>CSSを適用しないと、Figure 2のようになります。
</p><p>
<img alt="HTML&#x306B;&#x4F55;&#x3082;&#x9069;&#x7528;&#x3057;&#x3066;&#x3044;&#x306A;&#x3044;&#x4F8B;" src="/assets/public/0/05/examplewithoutHTML.png" width="655" height="192"/></p><p>Figure 2: 素のHTML。CSS スタイルは何も使っていません
</p><p>HTMLをデザインするCSSを見てみましょう。
</p>
<h3>styles.css</h3>
<pre class="css">
body {
  background: #fff url('images/gradbg.jpg') top left repeat-x;
  color: #000;
  margin: 0;
  padding:0;
  border: 0;
  font-family: Verdana, Arial, sans-serif; font-size: 1em;
}

div {
  width: 800px;
  margin: 0 auto;
}

#bggraphic {
  background: url('images/pen.png') top left no-repeat;
  height: 278px;
  width: 362px;
  position: absolute;
  left: 50%;
  z-index: 100;
}

h1 {
  text-align: center;
  text-transform: uppercase;
  font-size: 1.5em;
  margin-bottom: 30px;
  background: url('images/headbg.png') top left repeat;
  padding: 10px 0;
}

#references cite {
  margin: 1em 0 0 3em;
  text-indent: -3em;
  display: block;
  font-style: normal;
  padding-right: 3px;
}

.website {
  border-right: 5px solid blue;
}

.book {
  border-right: 5px solid red;
}

.article {
  border-right: 5px solid green;
}

#footer {
  font-size: 0.5em;
  border-top: 1px solid #000;
  margin-top: 20px;
}

#footer a {
  color: #000;
  text-decoration: none;
}

#footer a:hover {
  text-decoration: underline;
}

</pre>
<p><br/>
このページのデザインは、少々やり過ぎた感があります。CSSを使うことで実現できることを示すために、シンプルで分かりやすい背景にしています。
</p><p>1行目は、テキストと背景の色やテキスト周りのボーダーの幅のような、ドキュメントのデフォルトを設定しています。このようにわざわざ明示的にデフォルトを設定したくない方もいまるでしょう。また、最近のブラウザには自身のデフォルトを適用するものもあります。しかしデフォルトを設定するのは、良い考え方です。ブラウザが違っても、webサイトの見た目をよりコントロールできるようになります。
</p><p>次の行では、ページの幅を800ピクセルに設定しています(パーセントで指定すれば、ブラウザウインドウのサイズにもとづいて拡大・縮小できるようになるとはいえ)。マージンの設定は、ウインドウのセンターにコンテンツが置かれるようにしています。
</p><p>次にこのページの背景に注目してみましょう(<code>background: url</code> で修飾してあります)。このページに3種類の背景を用意しました。最初のものは、トップからブルーの諧調でタイル表示するものです。2番目は、ペンのPNG画像を半透明にしておいています。その上にテキストがあっても十分なコントラストで、諧調をとっています(半透明のPNG画像はInternet Explorer 6以前では表示できませんが、最近のブラウザではほとんど大丈夫です。<a rel="nofollow" class="external text" href="http://code.google.com/p/ie7-js/">Dean Edward's IE-fixing JavaScript</a>  には、IE6に対する解決策が載っています。これにはIE6のCSSサポートの問題のいくつかを解決する方法があります)。
</p><p>最後になりますが、ページ見出しの背景に半透明のPNGを使っています。これで見出しに少しコントラストがついて見やすくなっています。
</p><p>完全にスタイルを適用すると、Figure 3のようになります。
</p><p>
<img alt="&#x5B8C;&#x6210;&#x4F8B;" src="/assets/public/a/ab/final-html-and-css-example.jpg" width="650" height="270"/></p><p>Figure 3: スタイルを適用した完成例
</p>
<h2>デザインの現実</h2>
<p>気に留めておいてほしいことがあります。それは、ここで学んでいくweb標準は、理想である点です。webデザイナーと開発者がすべて、webサイトを作るのに最近のweb標準とベストプラクティスを使っていれば、そしてwebブラウザがみな現在のweb標準を完全にサポートしていれば、もっと物事は簡単だったでしょう。残念ながら、どちらもそうではありません。まず第一に、現在webサイトを作っているwebのプロたちは、多岐にわたる手段と様々な機会で作り方を学んできました。webサイトを作るのに、90年代後半に我々がしていたようなテーブルとスペーサーGIFといった悪習を、未だに使っている人もいます。ほとんどのwebのプロが独習であり、何かしらかの公的資格に関わってきた私たちでさえ、「正しい方法」で教えられたわけではありません。世間の大学のコースの多くは…こういってもかまわないと思いますが…時代遅れです。
</p><p>古い方法でやっている方とスキルの向上について話すことがあれば、おそらくこう言われるでしょう。「なんでそんなことしなければいけないんだ。私のやり方で動いてるし、新しいスキルを学ぶ時間なんてない。私は私のやり方でいくよ」。これはこれで理解できると思います。しかし、もし彼らがスキルを向上させる時間を持てれば、ブラウザに左右されないwebサイトの構築とコードをより簡単にメンテナンスできるようになることに、きっと気付くはずです。
さらに、アクセシビリティも向上し、おまけにSEOも。まずは、ここと同じようなコースで正しいやり方を学んで、やっていることが継続できるようになりましょう。もし他の方に最近のベストプラクティスを伝える機会ができれば、あなたはWebという世界に寄与したことになるでしょう。
</p><p>webブラウザのサポートについては、最近のブラウザはすべて、HTMLもCSSもJavaScriptもきちんと処理できます。問題は古いバージョンのInternet Explorerに対するレガシーな対応です。IE 6、7、8は、またかなりの数が使われています。webプロジェクトでこれらのサポートのために、あなたに招集がかかるかもしれません。様々な機能がサポートされていない状況を回避できることもありますし、サポート無しでまったく動かないというよりも(たとえ見栄えが悪くても)、なんとか動く状況もあるにはあります。
時と場合によりますが、これはまだましな方です。
</p><p>古いブラウザのサポートをどうするかについては、次の章で詳しく取り上げます。
</p>
<h2>サマリー</h2>
<p>HTMLとCSS、JavaScriptには何も神秘的な点はありません。単にwebが進化しただけです。すでにHTMLに取り組んでいるのなら、「捨て去る」ことは何もありません。知っていることすべてが現実の問題に直結しますので、手段を駆使して対処しなければいけません(マークアップには少し余計に注意を払って)。
</p><p>仕事がうまくいったという満足感を得ることはさておき、web標準にもとづいて開発は、当然なことです。標準にもとづいた開発に対しては、時間がかかること、どのブラウザでもうまくレイアウトできるようにすることが面倒になる、という反論があります。それに対して、広範囲なデバイスでなおかつ今後のブラウザのバージョンを非標準ベースでレイアウトすることに使えるのか、という反論があります。一体どうやって将来のOperaやFirefox、Safari、Chrome、Internet Explore等で、二重に大変なマークアップを表示させられると信じられるでしょうか? ルールに従わない限り、それは無理です。
</p><p><br/></p><p><br/></p><p><br/></p>
<h2>See also</h2>
<h3>External resources</h3>
<p><a rel="nofollow" class="external text" href="http://www.codecademy.com/tracks/web">Introduction to HTML &amp; CSS</a> - a practical course on the free e-Learning platform <a rel="nofollow" class="external text" href="http://www.codecademy.com">Codecademy</a>.
</p>
<h3>練習問題</h3>
<ul><li> classとIDの違いはなんですか?</li>
<li> webサイトでXHTMLとCSS、JavaScriptは、それぞれどのような役割を担いますか?</li>
<li> 例であげられたindex.htmlを使って、CSSだけを利用してフォーマットを変更してください(ファイルを修正するのには、NotepadやText Wranglerといったテキストエディターを使ってください)。HTMLは一切変更しないでください。
<ul><li> 文献の種類毎にアイコンを入れてください(文書・書籍・web上のリソース毎に違うアイコンで)。このために自分でアイコン作り、CSSだけを使って文献のタイプ毎に横に表示されるようにしてください。</li>
<li> ページ下部の著作権表示を隠してください。</li>
<li> タイトルを独自のものに変えてください。</li></ul></li>
<li> モバイルフォンのブラウザでこの例が動くようにするには、どのようなことをすればよいでしょうか?</li></ul>
