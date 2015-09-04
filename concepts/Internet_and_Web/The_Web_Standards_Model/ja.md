---
title: ja
tags:
  - Concept
  - Pages
summary: "concepts/internet_and_web/How_does_the_Internet_Workの続きです。 HTMLと CSS、JavaScript\nが取り入れられました。それではもう少し掘り下げて、この3つがwebサイトを作る際に何をしてどのように連携するのか、それぞれを見ていくことにしましょう。\n"
uri: 'concepts/Internet and Web/The Web Standards Model/ja'
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

---
# Web標準モデル HTMLとCSS、JavaScript

## Summary

concepts/internet\_and\_web/How\_does\_the\_Internet\_Workの続きです。 HTMLと CSS、JavaScript が取り入れられました。それではもう少し掘り下げて、この3つがwebサイトを作る際に何をしてどのように連携するのか、それぞれを見ていくことにしましょう。

## 分けた理由は?

web標準について質問されるもので、一番多いのがこれです。HTMLを使ってデザインとレイアウトをし、コンテンツを完成できます。フォント・エレメントはスタイルに使い、HTMLのテーブルはレイアウトに使いますが、どうしてXHTMLやCSSで悩む必要があるのでしょうか? レイアウトに使うテーブルなどは、webデザインがまだまだな過去において使われていましたが、いまだに使う人が大勢います(皆さんはそうしないで)。そもそもこのコースを作った理由の一つがこのためです。そのような方法はこのコースでは扱いません。ここでは旧式の方法に対して、CSSとHTMLを使う理由として、納得できるものをあげます。

1.  「効率的なコード」: ファイルが大きく長くなればなるほど、ダウンロードに時間がかかります。そうすると、見るのに時間がかかる人がいます(ダウンロードするのにメガバイト単位で課金される人もいます)。なので、HTMLファイル毎にデザインやレイアウトの情報をまき散らした大きなページで帯域を浪費したくないと考えるでしょう。HTMLファイルを必要最低限に整理し、デザインとレイアウトを独立した1つのCSSファイルとして、1回だけ取り込みましょう。このケースの実例をみるなら、[the A List Apart Slashdot rewrite article](http://www.alistapart.com/articles/slashdot/)です。ここでは、作者が著名なサイトをとりあげ、XHTMLとCSSで書き直しをしています。
2.  「メンテナンスが容易」: 引き続きになりますが、デザインとレイアウト情報を1か所にだけ指定しておけば、サイトのページの見た目を変更したい時に、1か所だけ更新すればよくなります。サイトのページ毎に情報を更新する方がよいですか? 私はそうは思いません。
3.  「アクセシビリティ」: 視覚に障害があるWebユーザは、「スクリーン・リーダー」というソフトウェアが使えます。これを使って、見た目ではなく音で情報にアクセスします。文字通り、ページを読んでユーザーへ伝えます。さらによいことには、そのページが見出しやパラグラフといったしっかりした意味構造を持っていれば、webページを案内することもできます。加えて、最良の方法で構築してあれば、webページでキーボードをコントロールすることさえできます(マウスが使えない運動障害をもった人にとって重要です)。

最後に、スクリーン・リーダーは、画像に組み込まれたテキストにはアクセスできず、JavaScriptを使ったものでも間違えてしまうことがあります。大事なコンテンツは誰にでも利用できるようにする、ということが大切です。

1.  「デバイス・コンパチビリティ」: HTMLやXHTMLが、デザインする情報がないシンプルなマークアップなら、ばらばらな属性(例えば、スクリーンサイズ)をもったデバイスたちでも、代わりとなるスタイルシートを適用するだけで再フォーマットできます。こうするのに方法はいくつかあります(この点については ([[mobile articles on dev.opera.com](http://dev.opera.com/articles/mobile/)] を参照してください)。CSSにも様々な体裁を整えるメソッドと、メディアタイプのためにスタイルシートを指定できるようになっています(例えば、スクリーンで見る、印刷する、モバイルデバイスで見る)。
2.  「Webクローラと検索エンジン」: 多分 Googleや他の検索エンジンが見つけやすいページを望んでいるのではないでしょうか。検索エンジンは「クローラ」という特殊なソフトウェアでページを読み回っています。クローラがページのコンテンツを見つけるのに支障が出たり、見出しを見出しとして定義していない等してしまい、何が重要なのかの判断を間違えてしまうと、恐らく適切な検索結果のランキングがおかしなことになってしまうでしょう。
3.  「よいものはよい」: 「俺が言ったんだから」的な理由ぽいです。しかし、プロで標準にあかるい開発者やデザイナーと話すと、コンテンツとデザイン、動作を分けることはwebアプリケーションの開発にとってベストだと言うでしょう。

## マークアップ、ページの基本

HTMLとXHTMLはマークアップ言語で、属性(オプションのものも必須のものもあります)をともなったエレメントで構成されています。エレメントは、ドキュメントの様々なタイプのコンテンツをマークアップするのに利用され、webブラウザでどの小さなコンテンツがレンダリングされるのかを指定します(例えば、見出しやパラグラフ、テーブル、箇条書き等)。

エレメントは、実際にコンテンツタイプを定義します。一方属性はエレメントについての追加情報を定義します。IDのようにエレメントを特定するものや、リンクがどこを指すのかを示す locationがあります。 マークアップはできるだけ意味を持たせるように心がけてください。つまり、コンテンツの機能を一意に表現するようにします。Figure 1 は代表的なエレメントの構造です。

![代表的なHTMLエレメント](/assets/public/6/62/article4-1.gif)

Figure 1: (X)HTML の構�

その点を考慮すると、HTMLとXHTMLの違いはどこにあるのでしょうか?

### XHTMLとは?

HTMLはもっとも古いweb言語で、webで見られる一番ありきたりなものです。厳しいシンタックスのルールと比べると、多少はルールが緩くなっています。それとは対照的に、XHTMLはXMLの語彙をもってHTMLを改善したものです。XMLは独自のマークアップ言語で、シンタックスのルールが厳しくなっています。XHTMLとHTMLの違いは、実際それほど大きいものではありません。あなたが将来、どこか癖のあるスタイルを持ったコーディング・ガイドラインを持ったどこかのwebチームで活動することになる場合を除けば。もしHTML5を使うのなら(このコースではそうしていきますが)、HTMLやXHTMLのシンタックスが使えます。

HTMLとXHTMLのシンタックス上の主な違い。 (引用元: [The web standards model](http://www.w3.org/community/webed/wiki/The_web_standards_model_-_HTML_CSS_and_JavaScript))

HTML:

-   エレメントと属性は、大文字・小文字の区別がありません。例えば、`<h1>` と `<H1>` は同じです。
-   閉じタグを必要としないエレメントがあります(例えば、paragraphs や `<p>`))。一方でその他(「空要素」という)は、閉じタグがありません(例えば、画像の `<img>`)。
-   属性値は、引用符で囲まなくても書ける場合があります。
-   ショートハンドが使える属性があります(つまり、`<input required>`)

XHTML:

-   エレメントと属性は、大文字・小文字の区別があります。全て小文字です。
-   エレメントはすべて、明示的に閉じなければいけません(例えば、`<p>A paragraph</p>`)。コンテンツがないエレメントは、開始タグ中でスラッシュを使って閉じなければいけません(例えば、`<hr></hr>` と

<!-- -->

    <hr/> は同じ意味です)。

-   属性は、引用符で囲まなければいけません。
-   全ての属性は、省略しない形式を使わなければいけません(`<input required="required">`)。

 Table 1: HTML と XHTML の違い

### 検証とは?

HTMLとXHTMLは標準なので(さらに言えば、CSSも)、the World Wide Web Consortium (W3C)はページを自動的にチェックするバリデーターという素晴らしいツールを作りました。このツールは、閉じタグ忘れや属性の引用符忘れといった、コードにある問題やエラーを指摘します。 [The HTML validator is available online](http://validator.w3.org/)は、HTMLかXHTMLどちらを使っているのか、どのドキュメントタイプを使っているのかを自動的に判定します。CSSをチェックしたいなら、[CSS validator を利用できます](http://jigsaw.w3.org/css-validator/) [HTML5 validator](http://html5.validator.nu/) というものもあり、W3CのものよりもHTML5関連については進んでいます。

検証についてさらに知りたいなら、[Validating your HTML](http://www.w3.org/wiki/Validating_your_HTML) を見てください。ドキュメントタイプについてさらに知りたいなら、[Choosing the right doctype for your HTML documents](http://www.w3.org/wiki/Choosing_the_right_doctype_for_your_HTML_documents) を見てください。

## CSS — スタイルを追加する

カスケーディング・スタイル・シートを使うと、ドキュメントの整形やレイアウトをうまくコントロールできます。体系的な規則にもとづいて処理を行い、スタイルしたいエレメントを選んで、エレメントの様々なプロパティに値を設定します。色や背景、フォントサイズ、スタイルを変更したり、追加したりできます。別の場所にあるwebページに設定することさえできます。これはCSSのルールの例です。

``` {.css}
p {
   line-height: 2;
   color: green;
}
```

`<p></p>` タグ内に囲まれたコンテンツは、2倍の行間でグリーンになります。

下記の例は、CSSがHTMLをどのようにデザインするのかについてヒントをくれるでしょう。さらにCSSを知りたいなら [CSS basics](http://www.w3.org/wiki/CSS_basics) から始めましょう。

## JavaScript — webページに動きを加える

最後になりますが、JavaScriptはwebページに動きをもたらすのに使うスクリプト言語です。フォームに入力したデータを検証したり(入力が正しいフォーマットかどうか、問い合わせる)、ドラッグ＆ドロップを実装したり、その場でスタイルを変更したり、メニューのようなエレメントを動かしたり、ボタンの機能を操作したりと、他にも山ほどの機能を用意しています。最近のJavaScriptは、ターゲットとなるHTMLの要素を見つけ出し、それに対して何かを働きかけます。まさにCSSと同じですが、操作もシンタックスも随分と違います。

JavaScriptは、HTMLやCSSと比べて複雑で範囲が広い課題です。なので、この段階で混乱を避けるために、シンプルなままにしておきます。このコースでは [Programming - the real basics](http://www.w3.org/wiki/Programming_-_the_real_basics) まで、JavaScriptは登場しません。

## 例のページ

カバーしてこなかった詳細なことは、たくさんあります。しかし、このwebデザインコースを通じて、全てを見ていきましょう! ここで実際のページ例をお見せして、この文書の残りで皆さんがすることになる雰囲気を感じ取ってください。

下記にあげた例は文献ページです。web開発チームにおける集団力学についての心理学のエッセーや米国におけるブロードバンド・インターネットの利用についての取り組みのレポートといった、主張したいことの最後に文献を引用するのに使えます。厳しい学術的なライティングにこだわるなら、この例はAPA形式(私はそれを取り上げざる得ない)で表現します。 [この例のHTMLとCSSが入ったzipファイルがダウンロードできます。](http://dev.opera.com/articles/view/4-the-web-standards-model-html-css-a/article4_examples.zip)

### index.html

``` {.html}
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
  <meta charset="utf-8"/>
  <title>References</title>
  <style type="text/css">
    @import url("styles.css");
  </style>
</head>
<body>
  <div id="bggraphic"></div>
  <div id="header">
    <h1>References</h1>
  </div>
  <div id="references">
    <cite class="article">Adams, J. R. (2008). The Benefits of Valid Markup: A Post-Modernistic
    Approach to Developing
    Websites. <em>The Journal of Awesome Web Standards, 15:7,</em> 57-62.</cite>
    <cite class="book">Baker, S. (2006). <em>Validate Your Pages.... Or Else!.</em>
    Detroit, MI: Are you out of your mind publishers.</cite>
    <cite class="article">Lane, J. C. (2007). Dude, HTML 4, that's like so 2000. <em>The
     Journal that Publishes Genius, 1:2, </em> 12-34.</cite>
    <cite class="website">Smith, J. Q. (2005). <em>Web Standards and You.</em>
    Retrieved May 3, 2007 from Web standards and you.</cite>
  </div>
  <div id="footer">
    <p>The content of this page is copyright © 2007 <a href="mailto:jonathan.lane@gmail.com">J. Lane</a></p>
  </div>
</body>
</html>
```

 このファイルを一行一行分析するつもりはありません。それは、これからいくつもの例を見ていくことになるからです。 しかしながら、代表的なものを次に取り上げます。

1行目は、ドキュメントタイプ宣言かドキュメントタイプというものです。この場合は、HTML5のページとなります。ドキュメントタイプのそもそもの考え方は、マークアップ言語に対して、守らなければならないルールを適用するというものでした。検証されても問題なく、実際全て満たしていれば、ブラウザは正確に「標準モード」でレンダリングできます。HTML5のドキュメントタイプは、この機能を実現するのに最も短い文字列です。ドキュメントタイプについてさらに詳しく知りたいなら、 [Choosing the right doctype for your HTML documents](http://www.w3.org/wiki/Choosing_the_right_doctype_for_your_HTML_documents) をご覧ください。

5\~7行目では、CSSファイルをページにインポートしています。このファイルに含まれたスタイルが、ページにある色々なエレメントへと適用されます。次のセクションでは、ページのフォーマットすべてを操作するCSSファイルの中身を見ることにします。異なる文献それぞれに別のクラスを割り当ててあります。こうすることで、文献のそれぞれのタイプに違うスタイルを適用できます。例えば、リストを検索しやすくするために、それぞれの文献の右側に違う色を付けました。

CSSを適用しないと、Figure 2のようになります。

![HTMLに何も適用していない例](/assets/public/0/05/examplewithoutHTML.png)

Figure 2: 素のHTML。CSS スタイルは何も使っていません

HTMLをデザインするCSSを見てみましょう。

### styles.css

``` {.css}
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
```

 このページのデザインは、少々やり過ぎた感があります。CSSを使うことで実現できることを示すために、シンプルで分かりやすい背景にしています。

1行目は、テキストと背景の色やテキスト周りのボーダーの幅のような、ドキュメントのデフォルトを設定しています。このようにわざわざ明示的にデフォルトを設定したくない方もいまるでしょう。また、最近のブラウザには自身のデフォルトを適用するものもあります。しかしデフォルトを設定するのは、良い考え方です。ブラウザが違っても、webサイトの見た目をよりコントロールできるようになります。

次の行では、ページの幅を800ピクセルに設定しています(パーセントで指定すれば、ブラウザウインドウのサイズにもとづいて拡大・縮小できるようになるとはいえ)。マージンの設定は、ウインドウのセンターにコンテンツが置かれるようにしています。

次にこのページの背景に注目してみましょう(`background: url` で修飾してあります)。このページに3種類の背景を用意しました。最初のものは、トップからブルーの諧調でタイル表示するものです。2番目は、ペンのPNG画像を半透明にしておいています。その上にテキストがあっても十分なコントラストで、諧調をとっています(半透明のPNG画像はInternet Explorer 6以前では表示できませんが、最近のブラウザではほとんど大丈夫です。[Dean Edward's IE-fixing JavaScript](http://code.google.com/p/ie7-js/) には、IE6に対する解決策が載っています。これにはIE6のCSSサポートの問題のいくつかを解決する方法があります)。

最後になりますが、ページ見出しの背景に半透明のPNGを使っています。これで見出しに少しコントラストがついて見やすくなっています。

完全にスタイルを適用すると、Figure 3のようになります。

![完成例](/assets/public/a/ab/final-html-and-css-example.jpg)

Figure 3: スタイルを適用した完成例

## デザインの現実

気に留めておいてほしいことがあります。それは、ここで学んでいくweb標準は、理想である点です。webデザイナーと開発者がすべて、webサイトを作るのに最近のweb標準とベストプラクティスを使っていれば、そしてwebブラウザがみな現在のweb標準を完全にサポートしていれば、もっと物事は簡単だったでしょう。残念ながら、どちらもそうではありません。まず第一に、現在webサイトを作っているwebのプロたちは、多岐にわたる手段と様々な機会で作り方を学んできました。webサイトを作るのに、90年代後半に我々がしていたようなテーブルとスペーサーGIFといった悪習を、未だに使っている人もいます。ほとんどのwebのプロが独習であり、何かしらかの公的資格に関わってきた私たちでさえ、「正しい方法」で教えられたわけではありません。世間の大学のコースの多くは…こういってもかまわないと思いますが…時代遅れです。

古い方法でやっている方とスキルの向上について話すことがあれば、おそらくこう言われるでしょう。「なんでそんなことしなければいけないんだ。私のやり方で動いてるし、新しいスキルを学ぶ時間なんてない。私は私のやり方でいくよ」。これはこれで理解できると思います。しかし、もし彼らがスキルを向上させる時間を持てれば、ブラウザに左右されないwebサイトの構築とコードをより簡単にメンテナンスできるようになることに、きっと気付くはずです。 さらに、アクセシビリティも向上し、おまけにSEOも。まずは、ここと同じようなコースで正しいやり方を学んで、やっていることが継続できるようになりましょう。もし他の方に最近のベストプラクティスを伝える機会ができれば、あなたはWebという世界に寄与したことになるでしょう。

webブラウザのサポートについては、最近のブラウザはすべて、HTMLもCSSもJavaScriptもきちんと処理できます。問題は古いバージョンのInternet Explorerに対するレガシーな対応です。IE 6、7、8は、またかなりの数が使われています。webプロジェクトでこれらのサポートのために、あなたに招集がかかるかもしれません。様々な機能がサポートされていない状況を回避できることもありますし、サポート無しでまったく動かないというよりも(たとえ見栄えが悪くても)、なんとか動く状況もあるにはあります。 時と場合によりますが、これはまだましな方です。

古いブラウザのサポートをどうするかについては、次の章で詳しく取り上げます。

## サマリー

HTMLとCSS、JavaScriptには何も神秘的な点はありません。単にwebが進化しただけです。すでにHTMLに取り組んでいるのなら、「捨て去る」ことは何もありません。知っていることすべてが現実の問題に直結しますので、手段を駆使して対処しなければいけません(マークアップには少し余計に注意を払って)。

仕事がうまくいったという満足感を得ることはさておき、web標準にもとづいて開発は、当然なことです。標準にもとづいた開発に対しては、時間がかかること、どのブラウザでもうまくレイアウトできるようにすることが面倒になる、という反論があります。それに対して、広範囲なデバイスでなおかつ今後のブラウザのバージョンを非標準ベースでレイアウトすることに使えるのか、という反論があります。一体どうやって将来のOperaやFirefox、Safari、Chrome、Internet Explore等で、二重に大変なマークアップを表示させられると信じられるでしょうか? ルールに従わない限り、それは無理です。

## See also

### External resources

[Introduction to HTML & CSS](http://www.codecademy.com/tracks/web) - a practical course on the free e-Learning platform [Codecademy](http://www.codecademy.com).

### 練習問題

-   classとIDの違いはなんですか?
-   webサイトでXHTMLとCSS、JavaScriptは、それぞれどのような役割を担いますか?
-   例であげられたindex.htmlを使って、CSSだけを利用してフォーマットを変更してください(ファイルを修正するのには、NotepadやText Wranglerといったテキストエディターを使ってください)。HTMLは一切変更しないでください。
    -   文献の種類毎にアイコンを入れてください(文書・書籍・web上のリソース毎に違うアイコンで)。このために自分でアイコン作り、CSSだけを使って文献のタイプ毎に横に表示されるようにしてください。
    -   ページ下部の著作権表示を隠してください。
    -   タイトルを独自のものに変えてください。
-   モバイルフォンのブラウザでこの例が動くようにするには、どのようなことをすればよいでしょうか?

**言語:**
:   **[English](/concepts/Internet_and_Web/The_Web_Standards_Model)**  • <span lang="ja">**日本語**</span>
