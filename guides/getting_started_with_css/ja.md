---
title: CSSの基礎
lang: ja
summary: 'このガイドでは，CSSの基礎（CSSの構造，セレクタ，コメント，HTMLへの適用方法を含む）をカバーしています．'
tags:
  - Guides
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'guides/getting started with css/af'
    - 'guides/getting started with css/ar'
    - 'guides/getting started with css/ast'
    - 'guides/getting started with css/az'
    - 'guides/getting started with css/bcc'
    - 'guides/getting started with css/bg'
    - 'guides/getting started with css/br'
    - 'guides/getting started with css/ca'
    - 'guides/getting started with css/cs'
    - 'guides/getting started with css/da'
    - 'guides/getting started with css/de'
    - 'guides/getting started with css/diq'
    - 'guides/getting started with css/el'
    - 'guides/getting started with css/eo'
    - 'guides/getting started with css/es'
    - 'guides/getting started with css/fa'
    - 'guides/getting started with css/fi'
    - 'guides/getting started with css/fr'
    - 'guides/getting started with css/gl'
    - 'guides/getting started with css/gu'
    - 'guides/getting started with css/he'
    - 'guides/getting started with css/hu'
    - 'guides/getting started with css/hy'
    - 'guides/getting started with css/id'
    - 'guides/getting started with css/it'
    - 'guides/getting started with css/ka'
    - 'guides/getting started with css/kk'
    - 'guides/getting started with css/km'
    - 'guides/getting started with css/ko'
    - 'guides/getting started with css/ksh'
    - 'guides/getting started with css/kw'
    - 'guides/getting started with css/mk'
    - 'guides/getting started with css/ml'
    - 'guides/getting started with css/mr'
    - 'guides/getting started with css/ms'
    - 'guides/getting started with css/nl'
    - 'guides/getting started with css/no'
    - 'guides/getting started with css/oc'
    - 'guides/getting started with css/pl'
    - 'guides/getting started with css/pt'
    - 'guides/getting started with css/pt-br'
    - 'guides/getting started with css/ro'
    - 'guides/getting started with css/ru'
    - 'guides/getting started with css/si'
    - 'guides/getting started with css/sk'
    - 'guides/getting started with css/sl'
    - 'guides/getting started with css/sq'
    - 'guides/getting started with css/sr'
    - 'guides/getting started with css/sv'
    - 'guides/getting started with css/ta'
    - 'guides/getting started with css/th'
    - 'guides/getting started with css/tr'
    - 'guides/getting started with css/uk'
    - 'guides/getting started with css/vi'
    - 'guides/getting started with css/yue'
    - 'guides/getting started with css/zh'
    - 'guides/getting started with css/zh-hans'
    - 'guides/getting started with css/zh-hant'
    - 'guides/getting started with css/zh-tw'
uri: 'guides/getting started with css/ja'

---
## <span>Summary</span>

このガイドでは，CSSの基礎（CSSの構造，セレクタ，コメント，HTMLへの適用方法を含む）をカバーしています．

## <span>はじめに</span>

この記事では，パワフルなスタイリング言語であるCSSを使い始めるにあたって助けとなる基本的な部分をカバーしています．HTML文書にCSSを適用する方法（`style`属性を使いインラインでスタイルを適用する方法，文書の`<head>`内で`<style>`要素でスタイルを埋め込む方法，当該文書の外部ファイルとして適用する方法）を学びます．

また，後者（`<link>`要素を使って外部スタイルシートにリンクする方法）が メンテナンスおよびキャッシュの点で最も理にかなっていることがわかると思います．

加えて，CSSの基本シンタックスの概要（コメントの付与，セレクタのタイプ，セレクタのグルーピングに関する詳細を含む）を提供します．

## <span>CSSとは?</span>

HTMLは文書を組み立てたり，ブラウザにページ要素（マークアップは例えば他のページへのリンクをさしたり，ページの見出しであることを示したりする）の機能を伝えたりする一方で， CSSはある要素を表示する方法（スタイリング，空白，色付けなど）をブラウザに指示するためのルールを提供します．

CSSのスタイルはルール（もしくはルールの集合）の系統により適用されます． CSSのルールに関する厳密なシンタックスを以下に述べます． CSSのルールは次のような感じです：

1.  どのHTML要素にスタイリングを適用すべきかを特定する
2.  スタイルが適用されたHTML要素の"プロパティ"（色，サイズ，フォント，及び他の属性）を明記する
3.  各プロパティの見栄えを制御するための値を含む

例えば，CSSのルールは次のように書かれます：

> ページ内の`<h2>`要素を全て見つけたい，そしてそのタグで囲まれたテキストの色を緑に変えたい.

や

> `author-name`のclass属性を持った全ての`<p>`要素を見つけたい．そして，背景色を赤にし，テキストのサイズを通常の段落の２倍にし，全方向の周辺に空白を10ピクセル付与したい．

のように．

CSSはJavaScriptのようなプログラミング言語ではないですし，HTMLのようなマークアップ言語でもありません－実際に，比較できるものがありません． Webが開発以前に定義されてきたインターフェースでは常に表現と構造（を示すインタフェース）が混ざっていました． 我々がコースの最初の方で話してきたように，Webと同じくらいしばしば変更される環境においてこれは賢くないのです．そこでCSSが開発されたわけです．

## <span>スタイルのルールに関する定義</span>

つべこべ言う前に，CSSのルールの例をレビューし，解明していこうと思います：

``` css
selector {
  property1:value;
  property2:value;
  property3:value;
}
```

 関連する部分は次のとおりです：

-   セレクタは，実際の要素名（例えば`<body>`）や他の識別子（例えば`class`属性の値）を使うことでルールによりどのHTML要素に影響を及ぼすのかを特定します．
-   波括弧"{}"にプロパティ／値の組を格納します．各組はお互いにセミコロン";"で分離します．プロパティと値はコロン":"で分離します．
-   プロパティは選択した要素に対し何をしたいのかを定義します．これらは多くの種類にわたっており，テキストの色や背景の色，ページ上の要素の位置，フォントタイプ，境界線の色や太さ，また他にも多くの見栄えやレイアウトの制御に関する属性に影響を及ぼします．
-   値は要素に適用された各プロパティの詳細を特定するための設定情報です．値はプロパティに依存します．例えば，色に影響を及ぼすプロパティは，\#336699のような感じで16進で示される色情報も使えますし，red，green，blueのような色の名前も使えます．位置，マージン，幅，高さ等に影響を及ぼすプロパティは，画素数（ピクセル），ems，パーセント，cm，他の単位で示されます．

以下の具体的な例を見てみましょう：

``` css
p {
  margin: 5px;
  font-family: arial;
  color: blue;
}
```

 このルールが影響を及ぼすHTML要素は`<p>`となります －さらなる特別なルールが適用されない限り，HTML文書中のすべての`<p>`，もしくは，このCSSのルールが適用される文書はこのスタイルで表示されるでしょう． より特別なルールが適用される場合はこのルールが上書きされます． このルールによって影響を及ぼすプロパティは段落の周辺のマージン，段落タグの中のテキストのフォント，そしてそのテキストの色です． マージンは5画素に，フォントはArialに，テキストの色は青にそれぞれ設定されています．

これらの詳細がすべて後の方でより細かく議論されます－このチュートリアルのメインゴールはCSSに関する細かな詳細を述べることよりも基礎をカバーすることです．

CSSルールのセット全体はスタイルシートを形成するためにCSS文書に付与されます．これはCSSルールを書く際に最も基本的なシンタックスです．いくつかのルールはもっと複雑ですが，そんなに多くはありません．おそらくCSSについて最もクールな方法は"簡単"にすることです．

### <span>CSSにおける空白文字の扱い</span>

CSSにおける空白文字はまさにHTMLの場合と同様な動作となることを注意してください． 余分な空白文字はCSSをレンダリングするブラウザによって完全に無視されますので，みなさんはコードを読みやすくするために好きなだけ多くの空白文字を入れることができます． そこで，このルール：

``` css
p {
  margin: 5px;
  font-family: arial;
  color: blue;
}
```

 はこのルール：

``` css
p {margin: 5px;font-family: arial;color: blue;}
```

 と機能的に等価です．異なる部分を分離するために必要な波括弧，コロン，セミコロンが含まれている限り，ブラウザはプロパティに適用する値を認識します．

### <span>CSSにおけるコメント</span>

早く知りたいことの一つにCSSでコメントを付与する方法があります． `/*` と `*/`で囲むことによりコメントを付与することができます． コメントは数行に渡ることもできます． ブラウザはテキストのコメント行を無視します．

``` css
/* These are basic element selectors */
selector{
  property1:value;
  property2:value;
  property3:value;
}
```

 あなたは，複数のルール間，もしくはプロパティブロックの中に，コメントを付与することができます． 例えば，次のCSSにおいて，２つ目ないし３つ目のプロパティをコメント用区切り文字で囲んだとしましょう．すると，それらはブラウザによって無視されます． これはあなたのWebページ上であるCSSのルールによる影響をテストする際に便利なのです． ただそれらをコメントアウトして，CSSファイルを保存し，ブラウザでHTMLページをリロードしてみましょう．

``` css
selector{
  property1:value;
  /*
  property2:value;
  property3:value;
  */
}
```

### <span>セレクタのグルーピング</span>

異なるセレクタのグルーピングも行えます．もし `h1` と `p`に同じスタイルを適用したいのであれば，次のようにCSSを書きます：

``` css
h1 {color:red;}

p {color:red;}
```

 ただ，同じ情報を繰り返していることから，この書き方は理想的ではありません．これを改善するために，コンマを使いセレクタをグルーピングすることでCSSを短くすることができます－これにより，波括弧内のルールが両方のセレクタに適用されます：

``` css
h1, p {color:red;}
```

### <span>セレクタの基本型</span>

いくつかの異なるセレクタが存在しており，それぞれがマークアップの異なる部分にマッチします．あなたが最もよく直面するであろう３つのタイプのセレクタは次のとおりです：

#### <span>要素型セレクタ</span>

``` css
p {}
```

 要素型セレクタはページ上のすべての要素にマッチします（上述のケースでは`<p>`要素）．HTMLタグを特定することにより，そのタグにより囲まれたページ内の全要素に影響を及ぼします． \</p\>

#### <span>class セレクタ</span>

``` css
.example {}
```

 classセレクタは，指定された値が付与された`class`属性を持つすべての要素にマッチするため，上記は`<p class="example">`, `<li class="example">`，`<div class="example">`, および，`example`の`class`が付与された全要素にマッチします．classセレクタはあらゆる要素名をtestしないことに注意してください．

#### <span>ID セレクタ</span>

``` css
#example {}
```

 IDセレクタは指定された値が付与された`id`属性を持つすべての要素にマッチするため， 上記は`<p id="example">`, `<li id="example">`，`<div id="example">`，および， `example`の`id`が付与された全要素にマッチします． IDセレクタはすべての要素名に対しテストされてないことに注意してください． HTML文書ごとにIDを１つずつ持つことができます－つまり，それらはページごとにユニークとなります．

次の例で上記のセレクタの動作例を見ることができます． ブラウザで下記の例をオープンすると，`warning`スタイルがitemとparagraphのリスト両方に適用されることに注意してください （もし中点が消えていたら，それは白い背景の上に白いテキストを設定しているためです）

-   [example-selectors.html](http://dev.opera.com/articles/view/27-css-basics/example-selectors.html)
-   [selectors.css](http://dev.opera.com/articles/view/27-css-basics/selectors.css)

#### <span>セレクタの結合</span>

特定のルールを定義するためにセレクタを結合することができます：

-   `p.warning {}` は，`warning`の`class`を持つすべての段落（p要素）にマッチします
-   `div#example {}` は，`example`という`id`属性を持つ要素にマッチします．ただし`div`のときのみです．
-   `p.info, li.highlight {}` は，`info` という`class`を持つ段落，および，`highlight`という`class`を持つlistアイテムにマッチします．

次の例では，いくつかのwarningスタイルの間で動作を識別するためにこれ（結合）を使っています：

-   [example-specificselectors.html](http://dev.opera.com/articles/view/27-css-basics/example-specificselectors.html)
-   [specificselectors.css](http://dev.opera.com/articles/view/27-css-basics/specificselectors.css)

## <span>CSSでの省略記法</span>

このコースにおいて，もう一つ定期的に出くわすと思われるのがCSSでの省略記法です． いくつかの関連するCSSプロパティを，時間や努力をセーブするために１つのプロパティに結合してしまうことが可能です． この節では，利用可能な省略記法のタイプについて見ていきましょう．

例えば，下記の`border`プロパティは省略記法で書かれたものです．

``` css
border: 2px solid black;
```

 これは以下と等価です．

``` css
border-width: 2px;
border-style: solid;
border-color: black;
```

### <span>個別の値と省略記法の場合の値との比較</span>

marginに関する以下のルールを考えます:

``` css
div.foo {
  margin-top: 1em;
  margin-right: 1.5em;
  margin-bottom: 2em;
  margin-left: 2.5em;
}
```

 このルールは次のようにも書けます：

``` css
div.foo {
  margin: 1em 1.5em 2em 2.5em;
}
```

 このプロパティでは４個未満の値を取ることもできます．次のようになります：

1.  上下左右で同じ値を適用 — `margin: 2px;`
2.  １個目の引数を上下の値，２個目の引数を左右の値としてそれぞれ適用 — `margin: 2px 5px;`.
3.  １個目の引数を上の値，３個目の引数を下の値，２個目の引数を左右の値としてそれぞれ適用 — `margin: 2px 5px 1px;`.

このように動作するプロパティがいくつかあります（`padding`, `margin`, `outline`を含め）．それについては後ほど明らかにします．

### <span>単一のプロパティを使うか省略記法の値を使うか</span>

省略記法の`margin`，`padding`プロパティは非常によく利用される傾向にありますが， 省略記法のプロパティは避けたほうが良い，もしくは，少なくとも注意深く検討したほうがよいシチュエーションがあります． 例えば次のようなシチュエーションです：

-   **単一のmarginを設定する必要がある場合** －プロパティを１つだけ設定する必要があるシチュエーションでは，複数のプロパティを同時に設定する行為は通常KISS（できるだけ簡単にしよう）の原理を妨害します．
-   **プロパティが適用するセレクタが多くの端点を対象とする場合**－

これが起こるとき（遅かれ早かれ起こるでしょうが），省略記法の値は当然ヒープが起こりますが， 修正するもしくはレイアウトを変えるという話になれば，フォローするのが難しくなりえます．

-   **あなたが書くスタイルシートが，限られたCSSのスキル（もしくは，空間推論の能力）を持つ人によりメンテナンスされる場合**－

彼らがこの記事を読むのであれば，このシナリオを心配する必要はないかもしれません．しかし，どんな仮説もベストではないでしょう．

-   **端点のケースを説明するために，値を変える必要がある**－

いい加減に設計された文書やスタイルシートでしばしば必要となりますが，それはほとんど聞きません．

## <span>HTMLへのCSSの適用</span>

CSSをHTML文書に適用する方法は３つあります：インラインスタイル，埋込みスタイル，そして外部スタイルシートです． もし，最初の２つのオプションを使う理由がないのであれば，常に３つ目のオプションを選択してください． その理由はすぐに明らかになるでしょう．しかし，ここでは種々のオプションの概要を示します．

### <span>インラインスタイル</span>

`style`属性を使って，次のように特定の要素にスタイルを適用することができます：

``` html
<p style="background:blue; color:white; padding:5px;">Paragraph</p>
```

 この属性の中に，すべてのCSSプロパティと値の組をリストアップします． それぞれのプロパティ／値の組は，お互いにセミコロンで区切られており，プロパティと値の間はコロンで区切られます．[このソース例を見てみてください](http://dev.opera.com/articles/view/27-css-basics/example-inline.html)．

ブラウザでこの例を見ると，`style`属性を持つparagraphが青地に白いテキストとなり，他とは異なるサイズになっています．これを図１に示します．

![Screenshot of the Opera browser showing an applied inline style sheet](/assets/public/7/7c/cssbasic.png)

図１: 他とは異なるインラインスタイルが適用されたparagraphをOperaで示した図

インラインスタイルの利点は，ブラウザが強制的にこの設定を使ってくれる点です． 他のスタイルシートで定義されたスタイルや文書の`<head>`に埋め込まれているスタイルがここで書かれたスタイルで上書きされます．

インラインスタイルにおける大きな問題は，メンテナンスがより大変な点です． CSSを使うことは構造から文書の表現部分を分離する点であるにもかかわらず，インラインスタイルはそれに逆行しています－文書を通して表現ルールを撒き散らしています

メンテナンスの問題に加えて，CSSにおける最もパワフルな点：カスケードを利用することができません．カスケードの概念は詳しくは後で述べますが， 今あなたが知っておくべきことは，カスケードを利用するというのは，あなたが一箇所でルック＆フィールを定義することで，それをブラウザがあるルールにマッチするすべての要素に適用してくれることを意味しています．

### <span>埋込みスタイル</span>

埋込みスタイルでは [この例のように](http://dev.opera.com/articles/view/27-css-basics/example-embedded.html) 文書の`<head>`に `<style>`要素が置かれます：

``` css
<style type="text/css" media="screen">
  p {
    color:white;
    background:blue;
    padding:5px;
  }
</style>
```

 上記のリンクをブラウザで見ると，図２に示すとおり，定義されたスタイルが文書中のすべてのparagraphに適用されていることがわかるでしょう．`head`の中にあるCSSを見るために，ページにあるソース例も見てみましょう．

![Screenshot of the Opera browser showing how an embedded style sheet affects a lot of elements](/assets/public/3/39/cssbasid.png)

図２：埋込みスタイルシートで定義されたスタイルを持つすべてのparagraphをOperaで示した図

埋込みスタイルの利点は，それぞれの段落に`style`属性を付与する必要がない点です－単一の定義だけでそれらすべてをスタイリングすることができます． これはもし全段落のルック＆フィールを変更する必要がある場合，１箇所だけ直せばよいことを意味します．ところが，これ（の及ぶ範囲）は１つの文書に限られます． では，もしサイト全体の段落の見栄えを１度で定義したいのならどうすればよいのか？ そのためには外部スタイルシートを使えばよいのです．

### <span>外部スタイルシート</span>

外部スタイルシートは自身のファイルにおけるCSSの定義すべてを置くことを意味します． 拡張子`.css`を持ったファイルを保存しておくことで． それから，文書の`<head>`の中に`<link>`要素を使ってそれをHTML文書に適用します． [ソース例のページ](http://dev.opera.com/articles/view/27-css-basics/example-external.html) をご覧下さい． `<head>`が，この [外部CSSファイル](http://dev.opera.com/articles/view/27-css-basics/styles.css) を参照する `<link>`要素を含んでいることに注意してください． 外部CSSファイルで定義されたスタイルがHTMLに適用されていることが検証できます．

``` html
<link rel="stylesheet" href="styles.css" type="text/css" media="screen">
```

`<link>`要素についてはこのコースの前で話してきました． 要約すると， `href`属性はCSSファイルを指し， `media`属性はどのメディアがこれらのスタイルを適用すべきかを定義し （プリントアウトがこのように見えて欲しくないような場合には`screen`）， `type`はリンクされたリソースが何であるかを定義します（ファイルの拡張子だけではそれを定義するのに十分でないためです）．

![Screenshot of the Opera browser showing how an external style sheet affects a lot of elements](/assets/public/1/1b/cssbasie.png)

図３：link要素でリンクされたとき，外部スタイルシートで定義されたスタイルをOperaブラウザで見たもの

これは想定内のすべてのケースにおいてベストなのです： ルック＆フィールの定義を単一のファイルで保持するためです． これは１つのファイルの変更がサイト全体を変えることを意味します， また，ブラウザはそれを一旦ロードすると，それを参照する他のすべて文書に対しキャッシュします．ダウンロードすることは意味がありません．

### <span>@importによるスタイルシートのインポート</span>

外部スタイルシートをHTMLファイルにインポートする方法がもうひとつあります－`@import`プロパティを利用する方法です． これは上述した埋め込まれたCSSと同じように埋込スタイルシートに挿入されます． シンタックスは次のような感じです：

``` html
<style type="text/css" media="screen">
  @import url("styles.css");

  ...他のインポート文やCSSスタイルがここに入り得る...

</style>
```

 インポート文はときどき括弧なしで書かれますが，同じ目的を達成できます． 他に気づくこととしては，`@import`が常に埋込スタイルシートの最初にある点です． また，インポートされたスタイルシートは，インポート文の最後にmedia typeを含むことによって，あるタイプのmediaにだけ適用されます (これはすべてのブラウザ（IE6以前を除く）で動作します). 次の文は前のコード例と同じになります：

``` html
<style type="text/css">
  @import url("styles.css") screen;

  ...他のインポート文やCSSスタイルがここに入り得る...

</style>
```

 あなたが最初の質問されることは「なぜ他に外部スタイルシートをHTML文書に適用する方法が必要なんだ？」でしょう． 主にここでは完全をきたすために`@import`に関する情報を含めています． `<link>`の上で`@import`を使うマイナーなメリット／デメリットが少しだけありますが，それらは非常にマイナーなので，どちらを使おうがあなた次第です． 今日，`<link>`要素が最も良い方法であると認識されています．

-   古いブラウザは`@import`を全く認識しないので，それを完全に無視します（Netscape 4以前およびIE4以前において，ファイル名から括弧を省いた場合）．

したがって，それらを不正に利用する古いバグだらけのブラウザからスタイルを隠蔽するために`@import`文を使うことができます． 外部スタイルシートにおいて更新されたスタイルや`@import`でインポートされたスタイルを置いた上で，埋込スタイルシートにおいてIE/Netscape 4に問題が生じる原因にはならない基本中の基本のスタイルを提供します． これは有益ではありますが，今日IE/Netscape 4の互換性が必要になるのはまれでしょう！

-   前述したとおり，IE6は`@import`行の後部にmedia typeを置く方法をサポートしていないので，異なるmediaに対し複数のスタイルシートを挿入したい場合，それらは良い方法ではありません．
-   複数の`@import`文に対するコードが複数の`<link>`要素に対するコードより小さいと主張するかもしれませんが，それは取るに足らないことです．

## <span>See also</span>

### <span>Other articles</span>

### <span>練習問題</span>

-   インラインスタイルの利点と問題点は何でしょうか？また，要素にどのように適用すればよいでしょうか？
-   スタイルルールとは何でしょうか？様々なコンポーネントやシンタックスを述べてください．
-   仮にスタイルルールのまとまりがあるとき，それらを外部スタイルシートに変えるために何をしないといけないでしょうか？
-   次のCSSセレクタは何にマッチするでしょうか？: `ul#nav{}`?
-   セレクタのグルーピングの利点は何でしょうか？
-   プリント用スタイルシートはどのように定義されていますか？
