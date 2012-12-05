{{Page_Title|CSSの基礎}}
{{Flags}}
{{Byline}}
{{Summary_Section|このガイドでは，CSSの基礎（CSSの構造，セレクタ，コメント，HTMLへの適用方法を含む）をカバーしています．}}
{{Guide
|Content=== はじめに ==

この記事では，パワフルなスタイリング言語であるCSSを使い始めるにあたって助けとなる基本的な部分をカバーしています．HTML文書にCSSを適用する方法（<code>style</code>属性を使いインラインでスタイルを適用する方法，文書の<code>&lt;head&gt;</code>内で<code>&lt;style&gt;</code>要素でスタイルを埋め込む方法，当該文書の外部ファイルとして適用する方法）を学びます．

また，後者（<code>&lt;link&gt;</code>要素を使って外部スタイルシートにリンクする方法）が
メンテナンスおよびキャッシュの点で最も理にかなっていることがわかると思います．

加えて，CSSの基本シンタックスの概要（コメントの付与，セレクタのタイプ，セレクタのグルーピングに関する詳細を含む）を提供します．

== CSSとは? ==

HTMLは文書を組み立てたり，ブラウザにページ要素（マークアップは例えば他のページへのリンクをさしたり，ページの見出しであることを示したりする）の機能を伝えたりする一方で，
CSSはある要素を表示する方法（スタイリング，空白，色付けなど）をブラウザに指示するためのルールを提供します．

CSSのスタイルはルール（もしくはルールの集合）の系統により適用されます．
CSSのルールに関する厳密なシンタックスを以下に述べます．
CSSのルールは次のような感じです：

#どのHTML要素にスタイリングを適用すべきかを特定する
#スタイルが適用されたHTML要素の"プロパティ"（色，サイズ，フォント，及び他の属性）を明記する
#各プロパティの見栄えを制御するための値を含む

例えば，CSSのルールは次のように書かれます：

<blockquote>ページ内の<code>&lt;h2&gt;</code>要素を全て見つけたい，そしてそのタグで囲まれたテキストの色を緑に変えたい.</blockquote>

や

<blockquote><code>author-name</code>のclass属性を持った全ての<code>&lt;p&gt;</code>要素を見つけたい．そして，背景色を赤にし，テキストのサイズを通常の段落の２倍にし，全方向の周辺に空白を10ピクセル付与したい．</blockquote>

のように．

CSSはJavaScriptのようなプログラミング言語ではないですし，HTMLのようなマークアップ言語でもありません－実際に，比較できるものがありません．
Webが開発以前に定義されてきたインターフェースでは常に表現と構造（を示すインタフェース）が混ざっていました．
我々がコースの最初の方で話してきたように，Webと同じくらいしばしば変更される環境においてこれは賢くないのです．そこでCSSが開発されたわけです．

== スタイルのルールに関する定義 ==

つべこべ言う前に，CSSのルールの例をレビューし，解明していこうと思います：

<syntaxhighlight lang="css">selector {
  property1:value;
  property2:value;
  property3:value;
}</syntaxhighlight>

関連する部分は次のとおりです：

*セレクタは，実際の要素名（例えば<code>&lt;body&gt;</code>）や他の識別子（例えば<code>class</code>属性の値）を使うことでルールによりどのHTML要素に影響を及ぼすのかを特定します．
*波括弧"{}"にプロパティ／値の組を格納します．各組はお互いにセミコロン";"で分離します．プロパティと値はコロン":"で分離します．
*プロパティは選択した要素に対し何をしたいのかを定義します．これらは多くの種類にわたっており，テキストの色や背景の色，ページ上の要素の位置，フォントタイプ，境界線の色や太さ，また他にも多くの見栄えやレイアウトの制御に関する属性に影響を及ぼします．
*値は要素に適用された各プロパティの詳細を特定するための設定情報です．値はプロパティに依存します．例えば，色に影響を及ぼすプロパティは，#336699のような感じで16進で示される色情報も使えますし，red，green，blueのような色の名前も使えます．位置，マージン，幅，高さ等に影響を及ぼすプロパティは，画素数（ピクセル），ems，パーセント，cm，他の単位で示されます．

以下の具体的な例を見てみましょう：

<syntaxhighlight lang="css">p {
  margin: 5px;
  font-family: arial;
  color: blue;
}</syntaxhighlight>

このルールが影響を及ぼすHTML要素は<code>&lt;p&gt;</code>となります
－さらなる特別なルールが適用されない限り，HTML文書中のすべての<code>&lt;p&gt;</code>，もしくは，このCSSのルールが適用される文書はこのスタイルで表示されるでしょう．
より特別なルールが適用される場合はこのルールが上書きされます．
このルールによって影響を及ぼすプロパティは段落の周辺のマージン，段落タグの中のテキストのフォント，そしてそのテキストの色です．
マージンは5画素に，フォントはArialに，テキストの色は青にそれぞれ設定されています．

これらの詳細がすべて後の方でより細かく議論されます－このチュートリアルのメインゴールはCSSに関する細かな詳細を述べることよりも基礎をカバーすることです．

CSSルールのセット全体はスタイルシートを形成するためにCSS文書に付与されます．これはCSSルールを書く際に最も基本的なシンタックスです．いくつかのルールはもっと複雑ですが，そんなに多くはありません．おそらくCSSについて最もクールな方法は"簡単"にすることです．

=== CSSにおける空白文字の扱い ===

CSSにおける空白文字はまさにHTMLの場合と同様な動作となることを注意してください．
余分な空白文字はCSSをレンダリングするブラウザによって完全に無視されますので，みなさんはコードを読みやすくするために好きなだけ多くの空白文字を入れることができます．
そこで，このルール：

<syntaxhighlight lang="css">p {
  margin: 5px;
  font-family: arial;
  color: blue;
}</syntaxhighlight>

はこのルール：

<syntaxhighlight lang="css">p {margin: 5px;font-family: arial;color: blue;}</syntaxhighlight>

と機能的に等価です．異なる部分を分離するために必要な波括弧，コロン，セミコロンが含まれている限り，ブラウザはプロパティに適用する値を認識します．

=== CSSにおけるコメント ===

早く知りたいことの一つにCSSでコメントを付与する方法があります．
<code>/*</code> と <code>*/</code>で囲むことによりコメントを付与することができます．
コメントは数行に渡ることもできます．
ブラウザはテキストのコメント行を無視します．

<syntaxhighlight lang="css">/* These are basic element selectors */
selector{
  property1:value;
  property2:value;
  property3:value;
}</syntaxhighlight>

あなたは，複数のルール間，もしくはプロパティブロックの中に，コメントを付与することができます．
例えば，次のCSSにおいて，２つ目ないし３つ目のプロパティをコメント用区切り文字で囲んだとしましょう．すると，それらはブラウザによって無視されます．
これはあなたのWebページ上であるCSSのルールによる影響をテストする際に便利なのです．
ただそれらをコメントアウトして，CSSファイルを保存し，ブラウザでHTMLページをリロードしてみましょう．

<syntaxhighlight lang="css">selector{
  property1:value;
  /* 
  property2:value;
  property3:value;
  */
}</syntaxhighlight>

=== セレクタのグルーピング ===

異なるセレクタのグルーピングも行えます．もし <code>h1</code> と <code>p</code>に同じスタイルを適用したいのであれば，次のようにCSSを書きます：

<syntaxhighlight lang="css">h1 {color:red;}

p {color:red;}</syntaxhighlight>
 
ただ，同じ情報を繰り返していることから，この書き方は理想的ではありません．これを改善するために，コンマを使いセレクタをグルーピングすることでCSSを短くすることができます－これにより，波括弧内のルールが両方のセレクタに適用されます：

<syntaxhighlight lang="css">h1, p {color:red;}</syntaxhighlight>

=== セレクタの基本型 ===

いくつかの異なるセレクタが存在しており，それぞれがマークアップの異なる部分にマッチします．あなたが最もよく直面するであろう３つのタイプのセレクタは次のとおりです：

==== 要素型セレクタ ====

<syntaxhighlight lang="css">p {}</syntaxhighlight>

要素型セレクタはページ上のすべての要素にマッチします（上述のケースでは<code>&lt;p&gt;</code>要素）．HTMLタグを特定することにより，そのタグにより囲まれたページ内の全要素に影響を及ぼします．
</p>

==== class セレクタ ====

<syntaxhighlight lang="css">.example {}</syntaxhighlight>

classセレクタは，指定された値が付与された<code>class</code>属性を持つすべての要素にマッチするため，上記は<code>&lt;p class="example"&gt;</code>, <code>&lt;li class="example"&gt;</code>，<code>&lt;div class="example"&gt;</code>, および，<code>example</code>の<code>class</code>が付与された全要素にマッチします．classセレクタはあらゆる要素名をtestしないことに注意してください．

==== ID セレクタ ====

<syntaxhighlight lang="css">#example {}</syntaxhighlight>

IDセレクタは指定された値が付与された<code>id</code>属性を持つすべての要素にマッチするため，
上記は<code>&lt;p id="example"&gt;</code>, <code>&lt;li id="example"&gt;</code>，<code>&lt;div id="example"&gt;</code>，および，
<code>example</code>の<code>id</code>が付与された全要素にマッチします．
IDセレクタはすべての要素名に対しテストされてないことに注意してください．
HTML文書ごとにIDを１つずつ持つことができます－つまり，それらはページごとにユニークとなります．

次の例で上記のセレクタの動作例を見ることができます．
ブラウザで下記の例をオープンすると，<code>warning</code>スタイルがitemとparagraphのリスト両方に適用されることに注意してください
（もし中点が消えていたら，それは白い背景の上に白いテキストを設定しているためです）

* [http://dev.opera.com/articles/view/27-css-basics/example-selectors.html example-selectors.html]
* [http://dev.opera.com/articles/view/27-css-basics/selectors.css selectors.css]

==== セレクタの結合 ====

特定のルールを定義するためにセレクタを結合することができます：

* <code>p.warning {}</code> は，<code>warning</code>の<code>class</code>を持つすべての段落（p要素）にマッチします
* <code>div#example {}</code> は，<code>example</code>という<code>id</code>属性を持つ要素にマッチします．ただし<code>div</code>のときのみです．
* <code>p.info, li.highlight {}</code> は，<code>info</code> という<code>class</code>を持つ段落，および，<code>highlight</code>という<code>class</code>を持つlistアイテムにマッチします．

次の例では，いくつかのwarningスタイルの間で動作を識別するためにこれ（結合）を使っています：

* [http://dev.opera.com/articles/view/27-css-basics/example-specificselectors.html example-specificselectors.html]
* [http://dev.opera.com/articles/view/27-css-basics/specificselectors.css specificselectors.css]

== CSSでの省略記法 ==

このコースにおいて，もう一つ定期的に出くわすと思われるのがCSSでの省略記法です．
いくつかの関連するCSSプロパティを，時間や努力をセーブするために１つのプロパティに結合してしまうことが可能です．
この節では，利用可能な省略記法のタイプについて見ていきましょう．

例えば，下記の<code>border</code>プロパティは省略記法で書かれたものです．

<syntaxhighlight lang="css">border: 2px solid black;</syntaxhighlight>

これは以下と等価です．

<syntaxhighlight lang="css">border-width: 2px;
border-style: solid;
border-color: black;</syntaxhighlight>

=== 個別の値と省略記法の場合の値との比較 ===

marginに関する以下のルールを考えます:

<syntaxhighlight lang="css">div.foo {
  margin-top: 1em;
  margin-right: 1.5em;
  margin-bottom: 2em;
  margin-left: 2.5em;
}</syntaxhighlight>

このルールは次のようにも書けます：

<syntaxhighlight lang="css">div.foo {
  margin: 1em 1.5em 2em 2.5em;
}</syntaxhighlight>
 
このプロパティでは４個未満の値を取ることもできます．次のようになります：

#上下左右で同じ値を適用 — <code>margin: 2px;</code>
#１個目の引数を上下の値，２個目の引数を左右の値としてそれぞれ適用 — <code>margin: 2px 5px;</code>.
#１個目の引数を上の値，３個目の引数を下の値，２個目の引数を左右の値としてそれぞれ適用 — <code>margin: 2px 5px 1px;</code>.

このように動作するプロパティがいくつかあります（<code>padding</code>, <code>margin</code>, <code>outline</code>を含め）．それについては後ほど明らかにします．

=== 単一のプロパティを使うか省略記法の値を使うか ===

省略記法の<code>margin</code>，<code>padding</code>プロパティは非常によく利用される傾向にありますが，
省略記法のプロパティは避けたほうが良い，もしくは，少なくとも注意深く検討したほうがよいシチュエーションがあります．
例えば次のようなシチュエーションです：

*'''単一のmarginを設定する必要がある場合''' －プロパティを１つだけ設定する必要があるシチュエーションでは，複数のプロパティを同時に設定する行為は通常KISS（できるだけ簡単にしよう）の原理を妨害します．
*'''プロパティが適用するセレクタが多くの端点を対象とする場合'''－
これが起こるとき（遅かれ早かれ起こるでしょうが），省略記法の値は当然ヒープが起こりますが，
修正するもしくはレイアウトを変えるという話になれば，フォローするのが難しくなりえます．
*'''あなたが書くスタイルシートが，限られたCSSのスキル（もしくは，空間推論の能力）を持つ人によりメンテナンスされる場合'''－
彼らがこの記事を読むのであれば，このシナリオを心配する必要はないかもしれません．しかし，どんな仮説もベストではないでしょう．
*'''端点のケースを説明するために，値を変える必要がある'''－
いい加減に設計された文書やスタイルシートでしばしば必要となりますが，それはほとんど聞きません．
<!--多分those are almost unheard ofだと思われます-->

== HTMLへのCSSの適用 ==
CSSをHTML文書に適用する方法は３つあります：インラインスタイル，埋込みスタイル，そして外部スタイルシートです．
もし，最初の２つのオプションを使う理由がないのであれば，常に３つ目のオプションを選択してください．
その理由はすぐに明らかになるでしょう．しかし，ここでは種々のオプションの概要を示します．

=== インラインスタイル ===

<code>style</code>属性を使って，次のように特定の要素にスタイルを適用することができます：

<syntaxhighlight lang="html5"><p style="background:blue; color:white; padding:5px;">Paragraph</p></syntaxhighlight>

この属性の中に，すべてのCSSプロパティと値の組をリストアップします．
それぞれのプロパティ／値の組は，お互いにセミコロンで区切られており，プロパティと値の間はコロンで区切られます．[http://dev.opera.com/articles/view/27-css-basics/example-inline.html このソース例を見てみてください]．

ブラウザでこの例を見ると，<code>style</code>属性を持つparagraphが青地に白いテキストとなり，他とは異なるサイズになっています．これを図１に示します．

[[Image:cssbasic.png|alt=Screenshot of the Opera browser showing an applied inline style sheet]]

図１: 他とは異なるインラインスタイルが適用されたparagraphをOperaで示した図

インラインスタイルの利点は，ブラウザが強制的にこの設定を使ってくれる点です．
他のスタイルシートで定義されたスタイルや文書の<code>&lt;head&gt;</code>に埋め込まれているスタイルがここで書かれたスタイルで上書きされます．

インラインスタイルにおける大きな問題は，メンテナンスがより大変な点です．
CSSを使うことは構造から文書の表現部分を分離する点であるにもかかわらず，インラインスタイルはそれに逆行しています－文書を通して表現ルールを撒き散らしています

メンテナンスの問題に加えて，CSSにおける最もパワフルな点：カスケードを利用することができません．カスケードの概念は詳しくは後で述べますが，
今あなたが知っておくべきことは，カスケードを利用するというのは，あなたが一箇所でルック＆フィールを定義することで，それをブラウザがあるルールにマッチするすべての要素に適用してくれることを意味しています．

=== 埋込みスタイル ===

埋込みスタイルでは [http://dev.opera.com/articles/view/27-css-basics/example-embedded.html この例のように] 文書の<code>&lt;head&gt;</code>に <code>&lt;style&gt;</code>要素が置かれます：

<syntaxhighlight lang="css"><style type="text/css" media="screen">
  p {
    color:white;
    background:blue; 
    padding:5px;
  }
</style></syntaxhighlight>

上記のリンクをブラウザで見ると，図２に示すとおり，定義されたスタイルが文書中のすべてのparagraphに適用されていることがわかるでしょう．<code>head</code>の中にあるCSSを見るために，ページにあるソース例も見てみましょう．

[[Image:cssbasid.png|Screenshot of the Opera browser showing how an embedded style sheet affects a lot of elements]]

図２：埋込みスタイルシートで定義されたスタイルを持つすべてのparagraphをOperaで示した図

埋込みスタイルの利点は，それぞれの段落に<code>style</code>属性を付与する必要がない点です－単一の定義だけでそれらすべてをスタイリングすることができます．
これはもし全段落のルック＆フィールを変更する必要がある場合，１箇所だけ直せばよいことを意味します．ところが，これ（の及ぶ範囲）は１つの文書に限られます．
では，もしサイト全体の段落の見栄えを１度で定義したいのならどうすればよいのか？
そのためには外部スタイルシートを使えばよいのです．

=== 外部スタイルシート ===

外部スタイルシートは自身のファイルにおけるCSSの定義すべてを置くことを意味します．
拡張子<code>.css</code>を持ったファイルを保存しておくことで．
それから，文書の<code>&lt;head&gt;</code>の中に<code>&lt;link&gt;</code>要素を使ってそれをHTML文書に適用します． [http://dev.opera.com/articles/view/27-css-basics/example-external.html ソース例のページ] をご覧下さい．
<code>&lt;head&gt;</code>が，この
[http://dev.opera.com/articles/view/27-css-basics/styles.css 外部CSSファイル] を参照する
<code>&lt;link&gt;</code>要素を含んでいることに注意してください．
外部CSSファイルで定義されたスタイルがHTMLに適用されていることが検証できます．

<syntaxhighlight lang="html5"><link rel="stylesheet" href="styles.css" type="text/css" media="screen"></syntaxhighlight>

<code>&lt;link&gt;</code>要素についてはこのコースの前で話してきました．
要約すると，
<code>href</code>属性はCSSファイルを指し，
<code>media</code>属性はどのメディアがこれらのスタイルを適用すべきかを定義し
（プリントアウトがこのように見えて欲しくないような場合には<code>screen</code>），
<code>type</code>はリンクされたリソースが何であるかを定義します（ファイルの拡張子だけではそれを定義するのに十分でないためです）．

[[Image:cssbasie.png|Screenshot of the Opera browser showing how an external style sheet affects a lot of elements]]

図３：link要素でリンクされたとき，外部スタイルシートで定義されたスタイルをOperaブラウザで見たもの

これは想定内のすべてのケースにおいてベストなのです：
ルック＆フィールの定義を単一のファイルで保持するためです．
これは１つのファイルの変更がサイト全体を変えることを意味します，
また，ブラウザはそれを一旦ロードすると，それを参照する他のすべて文書に対しキャッシュします．ダウンロードすることは意味がありません．

=== @importによるスタイルシートのインポート ===

外部スタイルシートをHTMLファイルにインポートする方法がもうひとつあります－<code>@import</code>プロパティを利用する方法です．
これは上述した埋め込まれたCSSと同じように埋込スタイルシートに挿入されます．
シンタックスは次のような感じです：

<syntaxhighlight lang="html5"><style type="text/css" media="screen">
  @import url("styles.css");

  ...他のインポート文やCSSスタイルがここに入り得る...

</style></syntaxhighlight>

インポート文はときどき括弧なしで書かれますが，同じ目的を達成できます．
他に気づくこととしては，<code>@import</code>が常に埋込スタイルシートの最初にある点です．
また，インポートされたスタイルシートは，インポート文の最後にmedia typeを含むことによって，あるタイプのmediaにだけ適用されます
(これはすべてのブラウザ（IE6以前を除く）で動作します). 
次の文は前のコード例と同じになります：

<syntaxhighlight lang="html5"><style type="text/css">
  @import url("styles.css") screen;

  ...他のインポート文やCSSスタイルがここに入り得る...
   
</style></syntaxhighlight>

あなたが最初の質問されることは「なぜ他に外部スタイルシートをHTML文書に適用する方法が必要なんだ？」でしょう．
主にここでは完全をきたすために<code>@import</code>に関する情報を含めています．
<code>&lt;link&gt;</code>の上で<code>@import</code>を使うマイナーなメリット／デメリットが少しだけありますが，それらは非常にマイナーなので，どちらを使おうがあなた次第です．
今日，<code>&lt;link&gt;</code>要素が最も良い方法であると認識されています．

* 古いブラウザは<code>@import</code>を全く認識しないので，それを完全に無視します（Netscape 4以前およびIE4以前において，ファイル名から括弧を省いた場合）．
したがって，それらを不正に利用する古いバグだらけのブラウザからスタイルを隠蔽するために<code>@import</code>文を使うことができます．
外部スタイルシートにおいて更新されたスタイルや<code>@import</code>でインポートされたスタイルを置いた上で，埋込スタイルシートにおいてIE/Netscape 4に問題が生じる原因にはならない基本中の基本のスタイルを提供します．
これは有益ではありますが，今日IE/Netscape 4の互換性が必要になるのはまれでしょう！
* 前述したとおり，IE6は<code>@import</code>行の後部にmedia typeを置く方法をサポートしていないので，異なるmediaに対し複数のスタイルシートを挿入したい場合，それらは良い方法ではありません．
* 複数の<code>@import</code>文に対するコードが複数の<code>&lt;link&gt;</code>要素に対するコードより小さいと主張するかもしれませんが，それは取るに足らないことです．
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links==== 練習問題 ===
*インラインスタイルの利点と問題点は何でしょうか？また，要素にどのように適用すればよいでしょうか？
*スタイルルールとは何でしょうか？様々なコンポーネントやシンタックスを述べてください．
*仮にスタイルルールのまとまりがあるとき，それらを外部スタイルシートに変えるために何をしないといけないでしょうか？
*次のCSSセレクタは何にマッチするでしょうか？: <code>ul#nav{}</code>?
*セレクタのグルーピングの利点は何でしょうか？
*プリント用スタイルシートはどのように定義されていますか？
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Languages}}









{{Languages}}