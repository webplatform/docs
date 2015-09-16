---
title: '画像の表示'
lang: ja
summary: 'この文書では、&lt;img&gt; タグを使って、HTMLドキュメントでの画像の利用について紹介します。'
tags:
  - Guides
  - CSS
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'guides/images in html/af'
    - 'guides/images in html/ar'
    - 'guides/images in html/ast'
    - 'guides/images in html/az'
    - 'guides/images in html/bcc'
    - 'guides/images in html/bg'
    - 'guides/images in html/br'
    - 'guides/images in html/ca'
    - 'guides/images in html/cs'
    - 'guides/images in html/da'
    - 'guides/images in html/de'
    - 'guides/images in html/diq'
    - 'guides/images in html/el'
    - 'guides/images in html/eo'
    - 'guides/images in html/es'
    - 'guides/images in html/fa'
    - 'guides/images in html/fi'
    - 'guides/images in html/fr'
    - 'guides/images in html/gl'
    - 'guides/images in html/gu'
    - 'guides/images in html/he'
    - 'guides/images in html/hu'
    - 'guides/images in html/hy'
    - 'guides/images in html/id'
    - 'guides/images in html/it'
    - 'guides/images in html/ka'
    - 'guides/images in html/kk'
    - 'guides/images in html/km'
    - 'guides/images in html/ko'
    - 'guides/images in html/ksh'
    - 'guides/images in html/kw'
    - 'guides/images in html/mk'
    - 'guides/images in html/ml'
    - 'guides/images in html/mr'
    - 'guides/images in html/ms'
    - 'guides/images in html/nl'
    - 'guides/images in html/no'
    - 'guides/images in html/oc'
    - 'guides/images in html/pl'
    - 'guides/images in html/pt'
    - 'guides/images in html/pt-br'
    - 'guides/images in html/ro'
    - 'guides/images in html/ru'
    - 'guides/images in html/si'
    - 'guides/images in html/sk'
    - 'guides/images in html/sl'
    - 'guides/images in html/sq'
    - 'guides/images in html/sr'
    - 'guides/images in html/sv'
    - 'guides/images in html/ta'
    - 'guides/images in html/th'
    - 'guides/images in html/tr'
    - 'guides/images in html/uk'
    - 'guides/images in html/vi'
    - 'guides/images in html/yue'
    - 'guides/images in html/zh'
    - 'guides/images in html/zh-hans'
    - 'guides/images in html/zh-hant'
    - 'guides/images in html/zh-tw'
uri: 'guides/images in html/ja'

---
## Summary

この文書では、&lt;img&gt; タグを使って、HTMLドキュメントでの画像の利用について紹介します。

## はじめに

この文書では、webのデザインを「快い」ものにすることを論じます。それは画像です。視覚障害を持った方でもサイトの情報を得られるように、利用しやすい方法でwebドキュメントの中に画像を追加するやり方を学んでいきます。情報を伝えるためにインライン画像をいつどのように使うのか、ページレイアウトをレベルアップするために、背景の画像をどうするのかも学んでいきます。

## 絵は千の言葉にとどまらない — それとも?

webサイトにはたくさんの画像を使いたくなります。画像は、訪問者にサイトの雰囲気を感じさせるとても良い手段ですし、図は目が見える学習者に複雑な情報を理解しやすくさせます。

webでの画像の欠点は、誰しもが画像を見られる訳ではないということです。ブラウザが初めて画像をサポートしたころを振り返ると、webの接続は遅く、オンラインでいるのに1分ごとにお金をたくさん使っていました。サイトの訪問者の多くは、画像表示を切ってダウンロードするコストを抑えつつ、webサーフィンを速くしていました。最近はこういうことはあまり見られませんが、それでも他にまだ考慮する問題があります。

-   モバイルデバイスでサーフィンしている方は、今でも画像を切っているかもしれません。理由はスクリーンが小さいことやデータのダウンロードのコストです。
-   サイトへの訪問者に、画像が正しく見えなかったり、全く見えなかったりする、視覚障害がある方がいるかもしれません。
-   異文化圏から来た訪問者がいるかもしれません。彼らは使用しているアイコンや図表を理解できません。
-   検索エンジンはテキストだけをインデックスします — 画像は分析しないので、画像にある情報は見つけられず、インデックスされません(少なくとも今のところは。最新の画像のインデックス化についての情報がさらに必要なら、試しに「画像のインデックス化」や「画像による検索」を検索してみてください)。

つまりとても大切なことは、よく考えて画像を選び、適切に使用することです。もっと大切なのは、画像を見られないユーザーのために、必ず代わりの手段を用意することです。

## コンテンツの画像と背景の画像

ドキュメントに画像を追加する主な方法は2つあります。`<img>` 要素を使ったコンテンツの画像とCSSを使って要素に当てはめた背景の画像です。どちらの方法を使うかは、みなさんの意図次第です。

-   画像が著者の写真やデータグラフといった、ドキュメントのコンテンツにとって極めて重要なものなら、`<img>` 要素として、画像の代わりとしてふさわしいテキストとともに追加してください。
-   画像がまさに見た目を配慮した目的で置かれているなら、CSSの背景画像を使用してください。この画像には画像の代わりとなるテキストは付けないでください(目が見えない方に対して「きらめく緑の角丸」という説明が何の役に立つ?)。そして、CSSで画像をデザインするやり方はいくつもあります。

## `<img>` 要素とその属性

画像を `<img>` 要素を使って、HTMLドキュメントに追加するのはとても簡単です。画像を表示したい場所を`src` (source) 属性の値として指定します。これでOKです。下記のHTMLドキュメントは、ブラウザでbalconyview.jpgを表示します(HTMLファイルと同じフォルダーから画像を読み込む)。

``` html
<!DOCTYPE html>

<html>
<head>
  <meta charset="utf-8">
  <title>Example of an inline image</title>
</head>
<body>
<img src="balconyview.jpg">
</body>
</html>
```

 このコードをブラウザで実行すると、結果はこのようになるでしょう。

![the image displayed in a browser](/assets/public/8/83/images-f.jpg)

*Figure 1: ブラウザで表示される画像*

注意点： `<img>` 要素は、いわゆる *空タグ* です。つまり終了タグが不要です(`</img>` のように)。HTML5では、内側のスラッシュで閉じることも必要ありません(\<img src="balconyview.jpg"/\> のように)。しかし、webページの作成者の多くは、他との釣り合いからそうしています。

### alt属性で画像の代わりになるテキストを用意する

画像を正しく表示しても、 `<img>` 要素が `alt` 属性を持っていなければ、HTMLとしては正しくありません。 この属性には、何らかの理由で画像が利用できない時に表示するテキストが入っています。画像が利用できない訳は、見つからない、ロードに失敗、ユーザーエージェント(普通はブラウザ)が画像をサポートしていない、といったものでしょう。さらに、視覚障害を持った方は支援技術を用いてwebページを読み上げています。この技術は、`alt` 属性のコンテンツを探しだし、画像を説明します。したがって、画像の内容を説明するためには、代わりとなるテキストを適切に書くことが重要です。アクセシビリティと検索エンジンの最適化のためにも、画像の `alt` 属性に、代わりとなるテキストを入れてください。

メモ書き：webページとその作成者の多くが、「altタグ」という用語を使っています。これは事実上正しくありません。そういった名前のタグ(もしくは要素)は存在しません。`alt` は `<img>` 要素の属性であって、タグではないことをお忘れなく。

したがって、画像を誰にでも理解できるようにするには、必ず代わりとなるテキストをこの例のように正しく付けなければいけません。

``` html
<!DOCTYPE html>

<html>
<head>
  <meta charset="utf-8">
  <title>Example of an inline image</title>
</head>
<body>
<img src="balconyview.jpg" alt="View from my balcony, showing a row of houses, trees and a castle">
</body>
</html>
```

### `title` 属性を使って「あればそれに越したことはない」情報を追加する

`alt` 属性には、画像が利用できない時に表示されるべきテキストを入れます。`alt` 属性内の情報は、画像がうまくロードされた時には表示されてはいけません。Internet Explorer はこの点が間違っていて、マウスポインタを画像に重ねるとツールチップとして表示します <sup>[[1]](#cite_note-1)</sup>。残念ながら、作成者の多くはこれがデフォルトだと見なして、画像についての追加情報を `alt` 属性に入れてしまっています。こうはしないでください。画像についての追加情報を加えたいなら、代わりに `title` 属性を使ってください。

たいていのブラウザは、`<img>` 要素の `title` 属性の値をマウスカーソルが重なった時に、ツールチップとして表示します(Figure 2参照)。これで訪問者はさらに画像について知りやすくなりますが、訪問者すべてがマウスを使うという前提はとれません。 `title` 属性はとても役に立ちますが、極めて重要な情報を示す確かな手段ではありません。それよりむしろ、画像の雰囲気や文脈での意味といった、本質的ではない情報を示すのに適した方法です。

``` html
<!DOCTYPE html>

<html>
<head>
  <meta charset="utf-8">
  <title>Example of an inline image with alternative text and title</title>
</head>
<body>
<img src="balconyview.jpg" alt="View from my balcony, showing a row of houses, trees and a castle"
  title="What I see when I look out of my window; the castle was one reason to move there.">
</body>
</html>
```

 このコードは、このようになります。

![title attribute contents shown as a tool tip](/assets/public/7/7c/images-g.jpg)

*Figure 2: `title` 属性は、多くのブラウザでツールチップとして表示される*

### `longdesc` を使って、複雑な画像の代わりを用意する <sup>[[2]](#cite_note-2)</sup>

図表や図形のように、画像がとても複雑な場合、`longdesc` 属性を使ってかなり長い説明を提供できます。そうすることで、スクリーンリーダーを使っている方や画像を切ってブラウジングしている方も、画像が伝える情報を利用できるようになります。

この属性には、同じ情報が含まれているHTMLドキュメントを指すURLが入ります。 例えば、一揃いのデータを表す図表があるとすると、`<longdesc>` を使って、同じ情報があるページへリンクすることができます。

``` html
<!DOCTYPE html>

<html>
<head>
  <meta charset="utf-8">
  <title>Example of an inline image with longdesc</title>
</head>
<body>
<img src="chart.png" width="450" height="150"
  alt="Chart showing the fruit consumption amongst under 15 year olds.
  Most children ate Pineapples, followed by Pears"
  longdesc="fruitconsumption.html">
</body>
</html>
```

 データファイルの「fruitconsumption.html」には、図表と同じデータを表すテーブルが入っています。

``` html
<!DOCTYPE html>

<html>
<head>
  <meta charset="utf-8">
  <title>Fruit consumption</title>
</head>
<body>
<table summary="Fruit Consumption of under 15 year olds, March 2007">
  <caption>Fruit Consumption</caption>
  <thead>
    <tr><th scope="col">Fruit</th><th scope="col">Amount</th></tr>
  </thead>
  <tbody>
    <tr><td>Apples</td><td>10</td></tr>
    <tr><td>Oranges</td><td>58</td></tr>
    <tr><td>Pineapples</td><td>95</td></tr>
    <tr><td>Bananas</td><td>30</td></tr>
    <tr><td>Raisins</td><td>8</td></tr>
    <tr><td>Pears</td><td>63</td></tr>
  </tbody>
</table>
<p><a href="inlineimagelongdesc.html">Back to article</a></p>
</body>
</html>
```

 並んで表示した2つの異なるデータは、このようになります。

![A document next to its longdesc output](/assets/public/f/f5/images-h.jpg)

*Figure 3: `longdesc` 属性を使って、画像にリンクした複雑なデータをともなったドキュメント*

注目して欲しいのは、画像に結びついた長い説明のファイルが存在するということを、見て分かる手掛かりがないことです。しかし、たいていの支援技術は、代わりとなるものが利用できることをユーザーに教えるでしょう。`longdesc` が無意味だと考える方もいるので、通常のリンク経由でリンクされた代替のページを用意してください。これがふさわしい場合も時にはあるかもしれません。なので、すべてのユーザーが情報に時間を割く方法を選べることが、効果的な場合がよくあります。しかし、デフォルトではテキストリンクを見せたくないケースもあるでしょう。

### 幅と高さを指定して大きさを決めることで、画像を速く表示する

ユーザーエージェントが `<img>` 要素をHTML中に見つけると、`src` 属性が指す画像をロードし始めます。 デフォルトでは画像の大きさは分かりませんので、すべてのテキストをひとまとめに表示し、画像が最終的にロードされて表示された時に、その周りに配置されます。こうなるとページのローディングが遅くなり、ページの訪問者にとって(控えめに言っても)見栄えが悪くなります。 これを防ぐには、 `width` と `height` 属性を使って画像の大きさを与え、画像をロードする前に画像用に正確なスペースを確保するようブラウザに伝えます。

``` html
<!DOCTYPE html>

<html>
<head>
  <meta charset="utf-8">
  <title>Example of an inline image with dimensions</title>
</head>
<body>
<img src="balconyview.jpg" alt="View from my balcony, showing a row of houses, trees and a castle"
  width="400" height="186">
</body>
</html>
```

 これは、画像が実際にロードされその場所に収まるまで、その画像と同じサイズのプレースホルダーを表示します。その結果、ページが見栄え悪く稚拙に変更されるのは避けられます。**必ず** 画像には `width` と `height` 属性を入れてください。

この属性を使えば、画像のリサイズも可能ですが(上記の例の属性値を半分にしてみてください)、うまいやり方ではありません。それはブラウザすべてで、画像をリサイズする質が滑らかではないからです。特に画像をリサイズし、サムネイルを表示する場合に不具合があります。サムネイルの目的が、実際の画像サイズよりも小さいというだけでなく、ファイルサイズもそうだからです。5KBも送れば十分な小さな画像を見るのに、300KBの写真をロードしたい人はいません。

## HTML5の \<figure\> を使って、画像をきちんと入れる

HTMLの画像に付きまとう問題の1つに、画像を入れる要素に何を選んだらよいのか、というものがあります。結局デフォルトで画像はインライン要素になります。この要素は前後で改行を強制しません。これはテキストの隣に小さなアイコンを置きたい場合には都合がよいのですが、ページに画像を行に渡って置きたい場合の方が多いのではないでしょうか。この使い方で表示するには、画像を単独の *figure* に入れます。

HTML4でこれを実現する最も一般的な方法は、画像を `<p>` か `<div>` 内に置くことです。しかし、どちらも最良の手段ではありません — 画像は段落ではありませんし、ブロック要素では意味がどうとでもとれます。HTML5の考案者はこれに気付き、問題を解決する新しい要素を導入しました。それが `<figure>` です。図を入れるよう特化して策定された要素で、画像が1つや2つもしくはマルチメディア要素の組み合わせ、テキスト、その他コンテンツが対象となります。例を見ていきましょう。

``` html
<!DOCTYPE html>

<html>
<head>
  <meta charset="utf-8">
  <title>Figure element with figcaption example</title>
  <style>
    figure,figcaption {
      display: block;
    }
  </style>
  <script>
    document.createElement('figure');
    document.createElement('figcaption');
  </script>
</head>
<body>
  <figure>
    <img src="balconyview.jpg" alt="View from my balcony, showing a row of houses,
      trees and a castle" width="400" height="186">
    <figcaption>The view from outside my window.</figcaption>
  </figure>
</body>
</html>
```

## HTML5の \<figcaption\> を使って、キャプションを正しく

HTML5に追加されたもう1つの新しい要素は、図のキャプションです。これまでは、`<p>` や別のまったく適切とは言えない要素を使って実装していましたが、現在は `<figcaption>` 要素があります。`<figure>` 内にネストさせます。「これはこの図の内容に関するキャプション」であることを示します。例は下記の通りです。

``` html
<!DOCTYPE html>

<html>

  ...

  <figure>
    <img src="balconyview.jpg" alt="View from my balcony, showing a row of houses, trees and a castle"
      width="400" height="186">
    <figcaption>The view from outside my window.</figcaption>
  </figure>

  ...

</html>
```

 注意して欲しいのは、図のキャプションが `alt` 属性や `title` 属性の内容を必ずしも置き換えるものではないということです。キャプションが画像のすべてを正確に説明しているのか、それとも `title` 属性が示すような補足的な情報なのかによります。この場合は、`alt` 属性も必要です。とうのは、目が見えるユーザーはそれを見ることで画像にあるものが見えるからです。The `alt` 属性は、見えないユーザーに対して画像の内容が何であるかを、正確に伝える手助けをしてくれます。一方キャプションは、文脈に沿った情報を加えます。

## CSSを用いた背景の画像

ブラウザがCSSをサポートし始めた時、webデザインが何倍も楽しくなったといっても過言ではありません。HTMLをハックして、テーブルのセルを使ってページに項目を配置したり、ノーブレークスペース(&nbsp;)を使って配置を強制したり、スペーサーGIF(透過な1x1ピクセルのGIF画像で余白を作るために伸縮される)を使ったりするかわりに、CSSでパディング・余白・大きさ・位置決めができます。そして、コンテンツの構造の気苦労をHTMLから取り除きます。

CSSを使うことで、とても融通が利く方法で背景の画像も使えるようになります。好きな方法でテキストの背景や周囲に画像を置くことができます。また、規則的なパターンで画像を繰り返して、背景を作成することもできます。終わりにする前に、CSSの画像について手短に取り上げます。

### CSSで背景を使用する方法

CSSで画像を背景として利用するのは、とても簡単です。下記のCSSコードを見る前にこの色々な例を見て、CSSにおいて背景の画像で可能な様々なことを知ってください。

![CSSの背景の例](/assets/public/e/ea/images-f.gif)

*Figure 4: CSSを使った背景*

ボックスは実際には `<h2>` 要素で整形されています。CSSにパディングとボーダーを設定し、 背景の画像用にスペースを確保しています。最初の例のCSSはこうなります。

``` css
background-image:url(ball.gif);
```

`background-image` プロパティを画像に加え、丸括弧内にURLを指定し、入れたい画像を指定します。 デフォルトでは、背景の画像は水平・垂直方向両方で繰り返され、最初の例のように項目すべてのスペースを埋めます。 しかし、 `background-repeat` プロパティを使えば、様々な繰り返しを仕組めます。

-   Don't repeat the image at all: `background-repeat:no-repeat;`
-   Only repeat the image horizontally: `background-repeat:repeat-x;`
-   Only repeat the image vertically: `background-repeat:repeat-y;`
-   画像の繰り返しはなし：`background-repeat:no-repeat;`
-   水平方向にだけ画像を繰り返す：`background-repeat:repeat-x;`
-   垂直方向にだけ画像を繰り返す：`background-repeat:no-repeat;`

デフォルトでは、背景の画像は(繰り返さなければ)、要素の左上に配置されるでしょう。 しかし、`background-position` を使えば、背景の画像をあちこちに動かせます。最も簡単に使用できる値は、垂直に調整するなら `top` と `center` 、`bottom`、水平に調整するなら `left` と `center`、 `right` です。例えば、画像を右下に配置するなら `background-position:right bottom;` を使い、画像を右側の垂直方向の中央にするなら `background-position:right center;` を使ってください。

背景の画像の繰り返しと配置を操作し、合わせて効果的な画像を使うことで、CSSがなかった時では不可能だった見事な効果をあげられます。そして、独立したCSSファイルに背景の設定を置いておくことで、ほんの数行コードを変更すれば、サイト全体の見た目をとても簡単に変更することができます。

## 結論

HTMLの画像は、非テキスト情報を提供するためのパワフルで柔軟な手段で、他のコンテンツの価値を向上させ、ページの見ための魅力を高めます。実証済みの手法と新しいHTML5の要素と属性を組み合わせることで、webページが確実に便利で面白く使いやすくなるようにできます。

## See also

### 練習問題

-   1280x786ピクセル大の画像があったとして、それを40x30ピクセルのサムネイルで表示したいとしたら、HTMLでそれができるか? またそうすることが良策か?
-   `longdesc` は何をする属性か? またブラウザはどう表示するか?
-   `valign` と `align` 属性は何をする属性か?またデフォルトではどう繰り返されるか?
-   要素の内で、CSSの背景の画像はデフォルトではどこに配置されるか? またデフォルトではどう繰り返されるか?

1.  <span class="mw-cite-backlink">[↑](#cite_ref-1)</span> <span class="reference-text">訳注：Internet Explorer 8からは、ツールチップを表示しません。詳しくは、 [[「What's New in Internet Explorer 8」の「Accessibility and ARIA」](https://msdn.microsoft.com/en-us/library/cc288472.aspx#access)] を参照してください。</span>
2.  <span class="mw-cite-backlink">[↑](#cite_ref-2)</span> <span class="reference-text"> 訳注： `longdesc` 属性は、ブラウザやスクリーンリーダーで実装があまり進んでいないようです。詳しくは [[アクセシビリティ・サポーテッド（AS）情報：H45](http://waic.jp/docs/jis2010-as-understanding/201406/H45.html)] を参照してください。</span>
