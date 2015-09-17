---
title: 'インターネットはどうなっている?'
lang: ja
summary: "時々舞台裏に回って、動作の陰に隠れた歯車やファンベルト見るようにうながされることがありませんか。今日あなたはラッキーです。この文書は、あなたがよくご存じのホットなテクノロジーの舞台裏に案内します。それは World Wide Web! ミュージック、スタート!\n"
tags:
  - Concept_Pages
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'concepts/Internet and Web/How does the Internet Work/af'
    - 'concepts/Internet and Web/How does the Internet Work/ar'
    - 'concepts/Internet and Web/How does the Internet Work/ast'
    - 'concepts/Internet and Web/How does the Internet Work/az'
    - 'concepts/Internet and Web/How does the Internet Work/bcc'
    - 'concepts/Internet and Web/How does the Internet Work/bg'
    - 'concepts/Internet and Web/How does the Internet Work/br'
    - 'concepts/Internet and Web/How does the Internet Work/ca'
    - 'concepts/Internet and Web/How does the Internet Work/cs'
    - 'concepts/Internet and Web/How does the Internet Work/da'
    - 'concepts/Internet and Web/How does the Internet Work/de'
    - 'concepts/Internet and Web/How does the Internet Work/diq'
    - 'concepts/Internet and Web/How does the Internet Work/el'
    - 'concepts/Internet and Web/How does the Internet Work/eo'
    - 'concepts/Internet and Web/How does the Internet Work/fa'
    - 'concepts/Internet and Web/How does the Internet Work/fi'
    - 'concepts/Internet and Web/How does the Internet Work/fr'
    - 'concepts/Internet and Web/How does the Internet Work/gl'
    - 'concepts/Internet and Web/How does the Internet Work/gu'
    - 'concepts/Internet and Web/How does the Internet Work/he'
    - 'concepts/Internet and Web/How does the Internet Work/hu'
    - 'concepts/Internet and Web/How does the Internet Work/hy'
    - 'concepts/Internet and Web/How does the Internet Work/id'
    - 'concepts/Internet and Web/How does the Internet Work/it'
    - 'concepts/Internet and Web/How does the Internet Work/ka'
    - 'concepts/Internet and Web/How does the Internet Work/kk'
    - 'concepts/Internet and Web/How does the Internet Work/km'
    - 'concepts/Internet and Web/How does the Internet Work/ko'
    - 'concepts/Internet and Web/How does the Internet Work/ksh'
    - 'concepts/Internet and Web/How does the Internet Work/kw'
    - 'concepts/Internet and Web/How does the Internet Work/mk'
    - 'concepts/Internet and Web/How does the Internet Work/ml'
    - 'concepts/Internet and Web/How does the Internet Work/mr'
    - 'concepts/Internet and Web/How does the Internet Work/ms'
    - 'concepts/Internet and Web/How does the Internet Work/nl'
    - 'concepts/Internet and Web/How does the Internet Work/no'
    - 'concepts/Internet and Web/How does the Internet Work/oc'
    - 'concepts/Internet and Web/How does the Internet Work/pl'
    - 'concepts/Internet and Web/How does the Internet Work/pt'
    - 'concepts/Internet and Web/How does the Internet Work/pt-br'
    - 'concepts/Internet and Web/How does the Internet Work/ro'
    - 'concepts/Internet and Web/How does the Internet Work/ru'
    - 'concepts/Internet and Web/How does the Internet Work/si'
    - 'concepts/Internet and Web/How does the Internet Work/sk'
    - 'concepts/Internet and Web/How does the Internet Work/sl'
    - 'concepts/Internet and Web/How does the Internet Work/sq'
    - 'concepts/Internet and Web/How does the Internet Work/sr'
    - 'concepts/Internet and Web/How does the Internet Work/sv'
    - 'concepts/Internet and Web/How does the Internet Work/ta'
    - 'concepts/Internet and Web/How does the Internet Work/th'
    - 'concepts/Internet and Web/How does the Internet Work/tr'
    - 'concepts/Internet and Web/How does the Internet Work/uk'
    - 'concepts/Internet and Web/How does the Internet Work/vi'
    - 'concepts/Internet and Web/How does the Internet Work/yue'
    - 'concepts/Internet and Web/How does the Internet Work/zh'
    - 'concepts/Internet and Web/How does the Internet Work/zh-hans'
    - 'concepts/Internet and Web/How does the Internet Work/zh-hant'
    - 'concepts/Internet and Web/How does the Internet Work/zh-tw'
translations:
  es:
    text: español
    href: /concepts/Internet_and_Web/How_does_the_Internet_Work/es
uri: 'concepts/Internet and Web/How does the Internet Work/ja'

---
## Summary

時々舞台裏に回って、動作の陰に隠れた歯車やファンベルト見るようにうながされることがありませんか。今日あなたはラッキーです。この文書は、あなたがよくご存じのホットなテクノロジーの舞台裏に案内します。それは World Wide Web! ミュージック、スタート!

この文書は World Wide Webを動かしている基盤となるテクノロジーをカバーしています。それは、

-   ハイパーテキスト・マークアップ言語(HTML)
-   ハイパーテキスト・トランスファー・プロトコル(HTTP)
-   ドメインネームシステム(DNS)
-   WebサーバとWebブラウザ
-   動的・静的コンテンツ

です。

ここに書いてあることが、webサイトをうまく構築するのに役立つ訳ではありません。それでも、お得意先など他の人と、きちんとWebについて話せるようになります。映画のサウンド・オブ・ミュージックで修道女から家庭教師になった賢い登場人物が次のように言いました。「文字を読むには、まずABCから始めますね。歌うのなら、ドレミから始めましょう」 この文書では実際にコンピュータがどのようにコミュニケーションをしているのかをざっとみてから、Webを構成するページを協調して作りあげている、色々な言語を見ていくことにします。

## コンピュータはどうやってインターネットでコミュニケーションをとっているのか?

コンピュータにとって、物事が複雑にならなかったのは幸いでした。World Wide Webが世に出た時、ほとんどのページは同じ言語で書かれました。それがHTMLです。HTMLはHTTPという共通のプロトコルを介してやりとりされました。HTTPは共通のインターネット言語(いくつかあり)で、例えば、Windowsマシンも最新の素晴らしいLinux(これこそドレミ!)が動作するマシンとハーモニーを奏でられます。HTTPを解釈しHTMLを描画するのに固有なソフトウェアであるwebブラウザを使えば、電話やPDA、ゲーム機といった色々なコンピュータを使って、どこでもHTMLで書かれたwebページを読めます。

コンピュータは同じ言語を話していますが、webにアクセスする様々なデバイス同士が話し合えるようになるには、ルールが必要になります。それは、教室で質問するために手を挙げるのと似ています。HTTPはインターネットに基本ルールをもたらしました。HTTPによって、クライアントマシン(皆さんのコンピュータのような)は、webページを見るためにリクエストを最初に出すものとみなされました。「サーバ」に対してまずリクエストを送ります。サーバとは、webサイト側にあるコンピュータです。webアドレスをブラウザに入力すると、サーバはそのリクエストを受け取り、望みのwebページを見つけます。そして皆さんのコンピュータへそのページを送り返し、webブラウザが表示します。

### リクエストとレスポンスのやりとりを分析する

それでは、コンピュータがインターネット越しに通信を行う全容を見ていきます。HTTPのリクエストとレスポンスのやりとりをさらに詳しく見ていくことにしましょう。良く理解できるように、いくつかのステップに分け、コンセプトのいくつかは、デモをして解りやすくします。

1.  リクエストとレスポンスは、URL(通常webアドレスとされています)をwebブラウザのアドレスバーに入力することで始まります。<http://www.apple.com> という感じです。さあここでブラウザを開いてください。そして、このURLを入力してエンターもしくはリターンすると(もしくは上記リンクをたどってください)、Appleのホームページに行きます。実はwebブラウザは、実際にはサーバに対してのリクエストにURLを使っていないことを皆さんは知らないかもしれません。ブラウザは「インターネット・プロトコル」もしくは「IPアドレス」を使っています(電話番号や宛名のように機能しますが、電話や住所よりもサーバを特定します。例えば、<http://www.apple.com> のIPアドレスは17.149.160.49です。
2.  ブラウザで新しいタブやウインドを開いて、<http://17.149.160.49/> とアドレスバーに入力してからエンターを押してみてください。ステップ１で見たのと同じページが見られるでしょう。

つまり、<http://www.apple.com> は <http://17.149.160.49/> のエイリアスとして機能しています。どうしてこうしているのでしょうか？ 理由は、長い数字を覚えるよりも単語を覚えた方が楽だからです。これを実現しているシステムをDNSと言い、インターネットにつながっている全てのマシンを自動で台帳化しています。<http://www.apple.com> とアドレスバーに入力すると、そのアドレスがDNSサーバに送られてマシンとIPアドレスを紐付けようとします。インターネットには、文字通り何百万ものマシンが接続されていますので、DNSサーバ毎にオンラインのマシン全ての一覧を保持している訳ではありません。リクエストを完了させるために他のDNSサーバで探すというシステムが整っているのです。最初のDNSサーバが分からなくても、これでリクエストが完了できます。DNSシステムはAppleのwebサイトを検索し、それが17.149.160.49であることを見つけ出して、webブラウザにIPアドレスを送ってきます。こうしてマシンはリクエストを指定されたIPアドレスに送り、返答が返ってくるのを待ちます。 全てがうまく行けば、サーバは全てOK、という短いメッセージ(Figure 1参照)をwebページの内容とともにクライアントに戻してきます。この種のメッセージは「HTTPヘッダー」に入ってます。

![リクエストとレスポンスの成功例](/assets/public/6/62/article3.gif)

Figure 1: このケースでは、全てがうまく行ってサーバは正しいwebページを返してきます。もし間違ったURLを入力してしまった、というような何か不都合があると、「HTTP error」がブラウザに返されてきます。悪名高き404 "page not found"エラーは、最もよく出会う例の一つです。

1.  <http://www.joniscool.co.uk/jonlane/> と入力してみてください。ページはありませんので、404エラーを受け取るはずです。ダミーのページをいくつか試してみて下さい。そうすると、違ったページが返ってくるのが見られます。これはwebの開発者がwebサーバに自分たちのデフォルトのエラーページを返すようにしているからです。存在しないページが返ってくると独自のエラーページが出るようにしている所もあります。これはさらに高度なテクニックなのでこのコースでは扱いませんが、Stuart Colville氏が素晴らしい文書を[Adding meaning to your HTTP error pages!](http://dev.opera.com/articles/view/adding-meaning-to-http-error-pages/) として公開しています。最後にURLについて。サイトを訪れる時の最初のURLには、実際のファイル名を最後に入れないのが普通です(例えば、 <http://www.mysite.com/> )。その続きのページもそうなっている場合もあれば、なっていない場合もあります。実際のファイルに必ずアクセスしているのですが、webの開発者はwebサーバにURLにファイル名が表示されないように設定している場合があります。これはURLを覚えるのに簡単で効果的な方法で、webサイトの利用者にとって好ましいことです。このコースではどうやってこうするのかは触れません。繰り返しますが、これはかなり高度なテクニックだからです。サーバにファイルをアップロードして、ファイルやフォルダーを構成するやり方は [Getting your content online](http://www.w3.org/community/webed/wiki/Getting_your_content_online)でCraig Grannell氏が触れています。

## コンテンツの種類

インターネットで出会うことになるコンテンツを見ていくことにしましょう。コンテンツは4つの種類に分けられます。それは、プレインテキストとweb標準、サーバサイド言語、アプリケーションやプラグインが必要とするフォーマットです。

### プレインテキスト

インターネットの黎明期、つまりweb標準もプラグインもまだないころは、画像とプレインテキストが大部分を占めていました。拡張子が.txtのようなファイルです。インターネットでプレインテキストに出会うと、ブラウザはそのまま表示します。そこには何の処理もありません。大学のサイトにはいまでもプレインテキストなファイルがよくあります。

### Web標準

World Wide Webの基本的な構成要素で頻繁に使われるweb標準は3つあります。それは、HTMLとCSS、JavaScriptです。

ハイパーテキスト・マークアップ言語は、コミュニケーションを目的としている限りは、なかなか評価が高いです。HTMLは、ドキュメントを分割してコンテンツと構造を規定し、それぞれの部分の意味を定義します(見出しやパラグラフ、箇条書き等)。エレメントを使ってページにある色々なコンポーネントを扱います。

カスケーディング・スタイル・シートを使えば、エレメントをどのようにデザインして配置するのかを全てコントロールできます。スタイル宣言を使えば、パラグラフ全てを変更して1行おきにしたり(`line-height: 2em;`)、レベル2の見出しをグリーンにしたり(`color: green;`)するのは簡単です。スタイルと構造を分離することはとてもメリットがありますので、[[in the next article](http://dev.opera.com/articles/view/4-the-web-standards-model-html-css-a/)]でもう少し細かく見ていきます。HTMLとCSSをいっしょに使って色々とできることを示すために、Figure 2では左側に全く整形していないシンプルなHTMLを表示し、一方右側にはCSSスタイルをきっちり適用したHTMLを示してあります。

![CSSを使用・未使用したHTMLのイメージ](/assets/public/6/6e/article4.gif)

Figure 2: 左はシンプルなHTMLで右はCSSを適用したHTML

最後になりますが、Javascriptはwebサイトやwebアプリケーションに動的な機能をもたらします。webブラウザで動くJavascriptプログラムを書くのに、特別なソフトウェアをインストールする必要はありません。Javascriptを使えば、強力な双方向性と動的な機能をwebサイトに導入できます。しかし制限がありますので、サーバサイド・プログラミング言語と動的webページが必要になります。

### サーバサイド言語

インターネットをブラウジングすると、.html拡張子ではなく.php,や.asp、.aspx、.jspといった見知らぬ拡張子を持ったwebページに出会う時があるでしょう。これらがサーバサイドのwebテクノロジーで、セクションがあるwebページを作る際に、webブラウザに表示するページを送る前に、変数の値によってページを変えています。例えば、動画リストのページは、データベースから動画の情報を取得して、日別・週別・月別といった動画の情報を表示したりできます。このタイプのwebページについては、下記の静的vs動的ページのセクションで扱います。

=== 他のアプリケーションやプラグインが必要なフォーマット

webブラウザは、web標準のような特定のテクノロジーを解釈して表示する機能をだけを持っています。ブラウザが解釈できないファイル・フォーマットやプラグインが必要なwebページを示すURLをリクエストすると、コンピュータにダウンロードするか、もしブラウザが既にプラグインを持っていれば、それを使って開きます。 例えば、

1.  WordやExcel、PDF、圧縮ファイル(ZIPやRAR)、Photoshop PSDのような複雑な画像ファイルといったブラウザが理解できないファイルに遭遇すると、ダウンロードするのかファイルを開くのか問い合わせてくるでしょう。どちらも結果は同じようになりますが、ファイルを開く方はファイルをダウンロードしてから、そのファイルを処理できるアプリケーションをインストールしてあれば、それで開く点が異なります。
2.  FlashムービーやJavaアプレット、処理できないミュージックビデオがあるページに出会うと、ブラウザはインストールされてあるプラグインがあれば、それを使って再生します。インストールしていなければ、必要になるプラグインをインストールするリンクが表示されるのが普通です。でなければ、ファイルがダウンロードされて、そのファイルを起動できるデスクトップアプリケーションを検索します。

はっきりしないところがあるのも事実です。例えば、ブラウザの中にはプレインストールされたプラグインが入っているものもあり、表示されたコンテンツがプラグインによるものなのかブラウザの元々のものなのか分からないものもあります。

## 静的vs動的ページ

静的と動的なwebサイトとはなんでしょうか。そしてその違いは? それはチョコレートを詰めた箱と似たようなもので、中に詰められています。

静的なwebサイトはコンテンツ(例えば、HTMLと画像コンテンツ)はいつも同じです。どの訪問者にも同じものを提供し、webサイトを作った人がサーバ上のコピーを自分で変更しようと決めない限り変わりません。これはまさに、これまで読んできたこの文書に当てはまります。

動的なwebサイトでは、サーバ上のコンテンツは似たようなものですが、HTMLに代わって動的なコードも入っています。動的なコードは、時刻やログインしたユーザ、日付、捜し物を見つけるために検索する言葉といった情報によって、違うデータを表示します。例を見てみましょう。webブラウザでwww.amazon.comに行き、別々の5つの製品を検索してください。Amazonは別々の5つのページは表示しません。ほとんど同じページを5回表示します。しかし毎回その中の情報は変化しています。データベースに異なる情報が記録されていて、リクエストが来ると関連する情報を持ってきます。それをwebサーバに渡して、動的なページに入れ込みます。

もう一つ注目したいことがあります。それは、特殊なソフトウェアがサーバにインストールされていて動的なwebサイトが作られているということです。普通の静的なHTMLはファイル拡張子を.htmlとして保存してあり、ブラウザは追加で他の助けを借りることなく処理できます。しかし、動的なページはHTMLに特別な動的コードを追加してあります。加えて、特定の拡張子をつけて保存し、クライアントに送る前にさらに処理が必要であることをwebサーバに伝えます(例えば、データベースから挿入されたデータがあるとか)。PHPファイルは通常は.phpという拡張子を持っています。

動的なwebサイトを動かしているサーバは、特別な動的コードを処理していますが、クライエントにはHTMLを送っています。クライエントは、特定のファイル拡張子のためのプラグインを用意する必要はありません。クライエントはHTMLファイルと似たようなものを受け取るからです。

私たちが選べる動的な言語とフレームワークは、たくさんあります。すでに紹介したPHPの他にもPythonやRuby on Rails、ASP.NET、Coldfusion等があります。 最後になりますが、これらのテクノロジーはほとんど同じ機能を持っています。例えば、データベースとのやり取りやフォームに入力された情報の検証等です。しかし少々異なる方法で実行し、それぞれ長所・短所があります。結局、自分に合ったものをということです。

このコースでは、動的言語についてはこれ以上触れません。でも、さらに詳しく知りたい方のために資料の一覧を用意しました。

-   Rails: Fernandez, Obie. (2007), The Rails Way. Addison-Wesley Professional Ruby Series.
-   [Rails screencasts](http://www.rubyonrails.org/screencasts)
-   PHP: Powers, David (2006), PHP Solutions: Dynamic web development made easy, friends of ED.
-   [PHP Online documentation](http://www.php.net/docs.php)
-   [PHP The Right Way](http://www.phptherightway.com/)
-   [The PHP League, a set of tested PHP packages using modern coding standards](http://thephpleague.com/)
-   ASP.NET: Lorenz, Patrick. (2003). ASP.NET 2.0 Revealed. Apress.
-   ASP.NET: [[online ASP.NET documentation and tutorials.](http://asp.net)]
-   [Backbone fundamentals](http://addyosmani.github.io/backbone-fundamentals)

## サマリー

インターネットがどのようになっているのか、舞台裏を見ていくのが目的です。この文書ではたくさんのトピックをカバーしていますが、ほんの少しかじるだけです。しかし、もやもやをとるのに役にたち、色々なテクノロジーが連携して動いているのが分かります。HTMLやCSS、Javascriptといった実際の言語のシンタックスについては、まだたくさん学ぶべきことがあります。それが次のステップになります。次の文書では、webの開発の「web標準」モデルであるHTMLやCSS、Javascriptに焦点を当て、webページのコードを見ていくことになります。

