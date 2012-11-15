{{Page_Title|HTML の <head> 要素}}
{{Flags}}
{{Byline}}
{{Summary_Section}}
{{Guide
|Content={{Languages}}

== はじめに ==

この記事は HTML 文書中であまり注目を集めない head 要素とその内容について説明します。このチュートリアルでは、DOCTYPE 宣言、title 要素、キーワードや説明 (meta 要素に記述します) など、head 要素の中身や関連する情報について説明します。また、JavaScript や CSS (内部で記述する方法と外部のものを参照する方法) についても説明します。

この記事ではサンプルをもとに解説するので、[http://dev.opera.com/articles/view/13-the-html-head-element/headtutorial.zip サンプルをダウンロード] して実際に試してみてください。私が説明するのは head 要素に関するベストプラクティスなので、ぜひチュートリアルを最初から最後まで進めてください。各パートはそれぞれ妥当なものではありますが、最後にいくつかそれまで教えたことを考え直させるような事も書いています。

== いったい &lt;head&gt; ってなに？ ==

<code>body</code> 要素は、文書のすべてのコンテンツを指定するための場所で、Webデザイナーやディベロッパーが多くの時間を費やす場所です。それに対して <code>head</code> 要素はあまり意味をなさないように見えます。なぜならこの要素の内容で、ページの利用者に直接現れるのは <code>title</code> 要素の情報だけだからです。これがどういう事かというと、<code>head</code> 要素は、ブラウザーに対する指定と、文書に関するメタ情報 (<code>meta</code>) など、付加的な情報を指定するための場所なのです。

== 文書の言語情報を指定する ==
 
文書に関する情報のうち、ひとつだけ head 要素の親、すなわち html 要素に指定するものがあります。文書の書かれている自然言語です。自然言語とはフランス語やタイ語、英語など人間が日常的に利用する言語を指します。自然言語情報を指定することで、スクリーンリーダーの手助けができるでしょう。たとえば、「six」という単語は英語とフランス語で発音が大きく異なります。こういった場合に自然言語情報はとても役立つのです。またスクリーンリーダー以外にも、検索エンジンなどがこの恩恵を受けられるのではないかと思います。

文書の主言語を指定することはよいことです。特に、世界に広く情報を公開するときにはとても役立ちます。あなたがそういったページを見ることはあまりないかもしれませんが。

言語情報は次のように指定します。
 
<syntaxhighlight lang="html5"><html lang="en-GB">
  ...
</html></syntaxhighlight>

言語情報を指定しないと、Googleやその他の検索エンジンは、Webサイトを見つけてクロールするのが困難になったり、予想以上に時間を要することがあります。
 
文書内の一部についても、この lang 属性を他の要素に与えることで言語情報を指定できます。たとえば、<span lang="fr">Bonjour</span> といったように書くことができます。
 
言語情報を指定する属性は、文書に指定した DOCTYPE によって変わります。 HTML のときは <code>lang</code> のみを、XHTML 1.0 を <code>text/html</code> で送出するときは <code>lang</code> と <code>xml:lang</code> を、XHTML を XML として扱うときは <code>xml:lang</code> のみを使います。

== タイトルが文書を評価する ==

<code>head</code> 内でもっとも重要なのが <code>title</code> 要素です。<code>title</code> 要素中に書かれたテキストは、すべてのブラウザーのタイトルバー (ウインドウ上部にある箇所) に表示されるからです。タイトルはあなたのサイトに訪れた人が最初に得る情報のひとつですから、とても重要なのです。

スクリーンリーダー (視覚障害者が利用することの多い、Web ページの内容を読み上げるソフトウェア) などの支援技術は、文書がどういう事柄に関するものなのかを利用者に知らせるため、文書のタイトルを利用します。また、検索エンジンも同様にタイトルを重要な情報として利用します。人に読みやすく、かつ内容をうまく伝えるキーワードを含む良いタイトルをつけられれば、あなたのページは多くの人に知られるようになるでしょう。

では、次のサンプル ([http://dev.opera.com/articles/view/13-the-html-head-element/headexample.html headexample.html]) を開いてみてください。
 
<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>I am a title example</title>
</head>
<body>
</body>
</html></syntaxhighlight>
 
図1 で示す通り、<code>title</code> 要素内のテキストが、ブラウザーのナビゲーションバーの上に表示されるのがわかると思います。

[[Image:Head-fig.gif|The title is displayed in the title bar of the web browser]] 

図1: ブラウザーでのタイトルの表示
 
良いタイトルのつけ方について Web には多くのチュートリアルがありますが、それらの殆どが SEO (検索エンジン最適化) に関連するものです。ですから、検索にたくさん引っかかるようなタイトルをつけるといった、検索エンジンへの対策に溺れないでください。文書が何について書かれているのかを、短く簡潔に表現しましょう。たとえば、「犬、ジャーマンシェパード、飼い方、ペット」と「犬の飼い方 ― ジャーマンシェパード」いうふたつのタイトルがあるとしします。いったいどちらが、訪問者にとってわかりやすいタイトルでしょうか。

== キーワードと説明を追加する ==
 
次に説明することは、あまり意味がないのではと思う人がいるかもしれません。指定する情報が、訪問者に対して直接表示されるわけではないからです。何のことかというと、ページの説明やキーワードです。これらの情報は head 内の meta 要素に与えます。では、Yahoo! Eurosport のサイト ([http://dev.opera.com/articles/view/13-the-html-head-element/headwithmeta.html headwithmeta.html]) を例にとって説明します。コードは次のように書かれています。
 
<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Yahoo! UK &amp; Ireland Eurosport—Sports News
|Sport</title>
  <meta name="description" content="Latest sports news and live scores from Yahoo! Eurosport UK. Complete sport coverage with Football results, Cricket scores, F1, Golf, Rugby, Tennis and more.">
  <meta name="keywords" content="eurosport,sports,sport,sports news,live scores,football,cricket,f1,golf,rugby,tennis,uk,yahoo">
</head>
<body>
</body>
</html></syntaxhighlight>
 
この文書をブラウザーで開いてみましょう。body になにも情報がないので、ブラウザーの画面には何も表示されないでしょう。しかし、この文書がオンラインにあり、検索エンジンがインデックスしていれば、ページの説明が検索結果の下に表示されることになります。図2 はそのスクリーンショットです。

[[Image:head-fih.gif|descriptions showing in a search engine results page]] 

図2: 検索結果でページの説明が表示されている
 
検索した人にとって、ページの説明はとても重要な情報になるでしょう。検索結果が表示してくれるページの説明を読んで、それが求めているページかを判断できるからです。また、いくつかのブラウザーは図3のように、ページをお気に入りに追加する際に、説明を補足情報として登録してくれる機能を備えています。

[[Image:head-fii.gif|Some browsers use the description as a bookmark description]] 

図3: 文書をお気に入りに登録する時、ブラウザーによっては記述されたページの説明も一緒に登録する
 
説明の追加は直接的な利益をもたらすものではありませんが、これらはあなたのページの成功に重要な役割を担います。説明より影響は大きくありませんが、キーワードについても同じことが言えます。

長年の spam 業者によるキーワードの不正利用によって、検索エンジンはキーワードを重要な情報として扱わなくなりました。それでも、キーワードはとてもよいツールになります。たとえば、多くの文書をすぐにインデックスしたい場合、キーワードがあればすべての文書をスキャンし内容を解析する必要がありません。meta キーワードをインデックスするスクリプトを用意し CMS の検索エンジンに利用すれば、検索が高速に行えるでしょう。内容を解析する必要なしに、文書を探し出す機能を手間なく導入できるのです。今はそういった機能を考えていなくても将来的に導入するチャンスが与えられると考えて、meta 要素にキーワードを与えることもよいのではないでしょうか。キーワードを分厚い本にはさむ小さなしおりとして考えてみましょう。しおりがあることで、長い章を読み返すことなく特定の節から読むことができるでしょう。

== 見た目は? スタイルを与えよう ==

<code>head</code> に与えられる情報はまだあります。CSS (Cascading Style Sheets) で定義されるスタイル規則です。スタイル規則は <code>style</code> 要素を使って <code>head</code> 要素内に直接埋め込めます。サンプル ([http://dev.opera.com/articles/view/13-the-html-head-element/headinlinestyles.html headinlinestyles.html]) は次のようになっています。
 
<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Breeding Dogs—Tips about Alsatians</title>
  <meta name="description" content="How to breed Alsatians, tips on proper breeding and information about common issues with this breed.">
  <meta name="keywords" content="Dogs,Alsatian,Breeding,Dog,Tips,Free,Pet">
  <style type="text/css">
    body{
      background:#000;
      color:#ccc;
      font-family: helvetica, arial, sans-serif;
    }
  </style>
</head>
<body>
<p>Test!</p>
</body>
</html></syntaxhighlight>
 
この文書をブラウザーで開くと、黒い背景のページに灰色で書かれた「Test!」という文字が現れるでしょう。また、書体はあなたのシステムにもよりますが、Helvetica または Arial で表示されるかと思います。<code>style</code> 要素は <code>media</code> という属性を持つことができますが、これはコンピューター画面やモバイル端末、印刷物など、媒体別にスタイルシートを適用させるための仕組みです。媒体にはいくつか種類がありますが、なかでも使われそうなものをここに挙げてみましょう。
 
* <code>screen</code> — ディスプレイやモニタ
* <code>print</code> — 文書が印刷されたときの見た目を定義する
* <code>handheld</code> — モバイル端末や他のハンドヘルド端末で表示させたときの見た目を定義する
* <code>projection</code> — [http://people.opera.com/howcome/2004/operashow/tutorial.html Opera Show] など、HTML によるスライドの表現に

たとえば、ディスプレイでは別の色を使って、印刷物ではフォントを大きくしたいといったとき、次のように <code>media</code> 属性に値 <code>print</code> を指定した新しいスタイルブロックを追加することで実現できます。(サンプルは [http://dev.opera.com/articles/view/13-the-html-head-element/headinlinestylesmedia.html headinlinestylesmedia.html] にあります)
 
<syntaxhighlight lang="html5"><style type="text/css" media="print">
  body{
    background:#fff;
    color:#000;
    font-family: helvetica, arial, sans-serif;
    font-size:300%;
  }
</style></syntaxhighlight>
 
この Web ページを印刷するとき、ブラウザーはスクリーン用スタイルシートではなく印刷用スタイルシートを適用します。サンプル [http://dev.opera.com/articles/view/13-the-html-head-element/headinlinestylesmedia.html headinlinestylesmedia.html] を開き、印刷プレビューを開いてください。図4 はそのスクリーンショットです。

[[Image:head-fij.gif|The same page with print and screen style sheets applied]] 

図4: スクリーン用スタイルシートと印刷用スタイルシート

== JavaScript で動的な機能を与えよう ==

head には他にも「クライアントサイドスクリプト」と呼ばれる、JavaScript で書かれたブラウザーによって実行されるスクリプトを追加することが出来ます。[http://www.w3.org/wiki/The_web_standards_model_-_HTML_CSS_and_JavaScript/ja Web 標準のモデル] で解説した通り、JavaScript は静的な HTML 文書に動的な挙動を与えるものです。たとえば、アニメーションやフォーム内容の検証など、ユーザーの行動に応じた反応が行えます。

JavaScript は script 要素を使って埋め込むことができます。ブラウザーがこの要素を見つけるとまず要素内のコードを実行し、その処理が終了するまで構文解析などの処理を中断します。つまり、ページの本文が表示される前に JavaScript を実行したい場合、その処理は head 内に記述する必要があります。たとえば、あなたのページに外部のサーバーへのリンクがいくつかあることをユーザーに伝えたい場合、次のようなコードを head 内に追加します。([http://dev.opera.com/articles/view/13-the-html-head-element/headscript.html headscript.html]): 
 
<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Breeding Dogs—Tips about Alsatians</title>
  <meta name="description" content="How to breed Alsatians, tips on proper breeding and information about common issues with this breed.">
  <meta name="keywords" content="Dogs,Alsatian,Breeding,Dog,Tips,Free,Pet">
  <style type="text/css" media="screen">
    body{
      background:#000;
      color:#ccc;
      font-family: helvetica, arial, sans-serif;
    }
    a {color:#fff}
  </style>
  <style type="text/css" media="print">
    body{
      background:#fff;
      color:#000;
      font-family: helvetica, arial, sans-serif;
      font-size:300%;
    }
  </style>
  <script>
    function leave(){
      return confirm("This will take you to another site,\n are you sure you want to go?")
    }
  </script>
</head>
<body>
Test!
<a href="http://dailypuppy.com" onclick="return leave()">The Daily Puppy</a>
</body>
</html></syntaxhighlight>
 
ブラウザーでこのサンプルを開き、リンクをクリックすると、外部サーバーに移動してよいかと訪ねてくるはずです。これはとても単純なスクリプトのサンプルとして用意しただけなので、ベストプラクティスではまったくありません。JavaScript のベストプラクティスや JavaScript の詳細なテクニックについては、後の記事で解説します。でも、いまは焦らずにいきましょう。

== インラインな CSS や JavaScript は良くない ==

強い言葉を書きましたが、Web サイトを構築する時に覚えておいてほしいことがひとつあります。コードを可能な限り再利用できるようにすると最もよいです。サイト全体で利用されるスタイルシートやスクリプトを各ページに埋め込むのは意義のあることではありません。それどころか、サイト全体を管理することが大変になりますし、文書のサイズも不必要に大きくなってしまいます。

スタイルシートやスクリプトは外部ファイルに格納し、必要に応じて HTML ファイルから読み込む方がずっとよいやり方です。こうすることで、変更が必要な場合でも、その外部ファイルを編集するだけで済むからです。JavaScript の場合、<code>script</code> 要素内には何も書かず、<code>src</code> 属性から外部ファイルにリンクします。コードは次のようになります。([http://dev.opera.com/articles/view/13-the-html-head-element/externaljs.html externaljs.html])
 
<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Breeding Dogs—Tips about Alsatians</title>
  <meta name="description" content="How to breed Alsatians, tips on proper breeding and information about common issues with this breed.">
  <meta name="keywords" content="Dogs,Alsatian,Breeding,Dog,Tips,Free,Pet">
  <style type="text/css" media="screen">
    body{
      background:#000;
      color:#ccc;
      font-family: helvetica, arial, sans-serif;
    }
    a {color:#fff}
  </style>
  <style type="text/css" media="print">
    body{
      background:#fff;
      color:#000;
      font-family: helvetica, arial, sans-serif;
      font-size:300%;
    }
  </style>
  <script src="leaving.js"></script>
</head>
<body>
Test!
<a href="http://dailypuppy.com" onclick="return leave()">The Daily Puppy</a>
</body>
</html></syntaxhighlight>
 
CSS の場合はすこし難しくなります。<code>style</code> は <code>src</code> 属性を持たないため、代わりに <code>link</code> 要素を利用することになります。<code>link</code> 要素は <code>href</code> 属性から外部 CSS を読み込むことができます。また、画面用か印刷用かを指定したい場合には <code>media</code> 属性が用意されています。CSS と JavaScript を固有のファイルに格納することにより、<code>head</code> 要素の長さをとても短くすることができます。([http://dev.opera.com/articles/view/13-the-html-head-element/externalall.html externalall.html])
 
<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Breeding Dogs—Tips about Alsatians</title>
  <meta name="description" content="How to breed Alsatians, tips on proper breeding and information about common issues with this breed.">
  <meta name="keywords" content="Dogs,Alsatian,Breeding,Dog,Tips,Free,Pet">
  <link rel="stylesheet" type="text/css" media="screen" href="styles.css">
  <link rel="stylesheet" type="text/css" media="print" href="printstyles.css">
  <script src="leaving.js"></script>
</head>
<body>
Test!
<a href="http://dailypuppy.com" onclick="return leave()">The Daily Puppy</a>
</body>
</html></syntaxhighlight>
 
スタイルシートとスクリプトを外部ファイルにする利点は、他にもあります。

# ページを速く表示させることができ、訪問者にやさしいつくにりなります。ダウンロードするファイルはすこしですが、共通に利用するスタイルシートやスクリプトを毎回読み込む必要はありません (外部スクリプト/スタイルシートは一度のダウンロードで済みます)。加えて、リンクした CSS ファイルと JavaScript ファイルはキャッシュされます (コンピューターに一時的に保存されます)。次にサイトにアクセスしたとき、その CSS ファイルと JavaScript ファイルはあなたのコンピューターに既に存在しているため、再びダウンロードする必要がありません。
# メンテナンスが容易になります。数千ページからなるサイトでも、スタイルシートとスクリプトが一箇所にあれば、なにか変更したい場合でもひとつひとつのファイルを編集する必要はありません。
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections=== 課題 ==

* スクリーンに表示されないのに、meta 要素にサイトの説明を加える意義はなんでしょうか。
* JavaScript を body ではなく head 内に追加することの利点はなんでしょうか。
* ブラウザーのキャッシュ機能の利点はなんでしょうか。そして、その恩恵を得るためには何をすればいいでしょうか。
* 検索エンジンが文書のタイトルを重要視しているなら、関連するキーワードをすべて記述した方がよいのでしょうか。なにかこのやり方に問題はありますか？
* タイトルの表示が少しつまらないので、b 要素でいくつかを太字にさせたいと思うのですが、これは可能ですか？

}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}