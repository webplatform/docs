{{Page_Title|HTMLの基礎}}
{{Flags}}
{{Byline}}
{{Summary_Section}}
{{Guide
|Content={{Languages}}

== はじめに ==

== HTML とは ==
 
ほとんどのソフトウェアは、専用のファイル形式を読み書きします。たとえば、Microsoft Word は “.doc” ファイルに対応し、Microsoft Excel は “.xls” に対応します。これらのファイルには文書内容のほかに、次に開いた時の再構築の手順を記す情報、「メタデータ」と呼ばれる文書に関する情報が格納されています。メタデータには、文書の執筆者や最終変更日、新旧のバージョンを行き来するための変更履歴などが含まれています。

[[html|HTML (“HyperText Markup Language”)]] は Web 文書の内容を記述する言語になります。HTML の構文では「要素 (elements)」と呼ばれる仕組みを利用します。要素は文書中のテキストを囲み、ユーザーエージェントにその箇所がどのような挙動をとればよいかを伝えるのです。

ここでは「Web ブラウザー」という言葉にかわり「ユーザーエージェント」という技術用語を使っています。ユーザーエージェントは、ユーザーのかわりに Web ページにアクセスするソフトウェア全般を指し示す言葉です。デスクトップブラウザー (Internet Explorer, Opera, Firefox, Safari など) やその他のデバイス用のブラウザー (Wii インターネットチャンネルや、Opera Mini, iPhone WebKit に代表されるモバイルブラウザー) は、もちろんユーザーエージェントになります。

しかし、ここで重要なのは、ブラウザーだけがユーザーエージェントではないということです。たとえば、Google や Yahoo! が自社の検索エンジンのために利用する、Web の自動インデックスプログラムもユーザーエージェントになります (ただし、この場合は人間が直接プログラムを操作することはありません)。

== HTML はどんなもの？ ==

HTML は文書の内容とその意味をプレーンテキストで表すフォーマットです。たとえば、以下のようなものです。

<syntaxhighlight lang="html5"><p id="example">ここは段落です。</p></syntaxhighlight>

この “<code>&lt;p&gt;</code>” という部分は段落を表すしるし (「開始タグ」と呼びます) になり、この場合は「このあとに続く部分を段落として扱う」という意味になります。そして、“<code>&lt;/p&gt;</code>” は段落を終了するタグ (「終了タグ」と呼びます) になります。

「要素」とは、開始タグから、開始タグから終了タグの間にある内容と、終了タグまでを含めた箇所を指します。開始タグの中にある <code>id="example"</code> は属性といいます。これについては後ほど説明します。多くの人が要素の意味で「タグ」という言葉を使用しています (前述したとおり、これは厳密には正しくありません)。
 
多くのブラウザーには「ソース」または「ソースを表示」という機能が搭載されており、たいていの場合「表示」メニューから選択することができます。もし、あなたの利用するブラウザーがソース表示機能を提供していたら、選択してページの HTML ソースをしばらく眺めてみましょう。


== HTML のあゆみ ==

[[The_history_of_the_Web/ja|インターネットと Web の歴史]] では、どのように Web が成立したかその歴史が語られています。そしてそこには、Tim Berners-Lee が World Wide Web を発明したとき、彼は最初の Web サーバーと Web ブラウザー、そして [http://www.w3.org/History/19921103-hypertext/hypertext/WWW/MarkUp/MarkUp.html HTML の最初のバージョン] を作成したことが書かれています。

現在の HTML は、その初期のバージョンから大きく変化していますが、多くの内容は現在の HTML にも生きています。また、初期のバージョンに存在した「タグ」の半分以上は、今でも使われ続けています。

多くの人が Web ページを書き始め、最初のブラウザー以外にブラウザーが登場するようになってから、多くの機能が HTML に追加されていきました。そのうちの多くは広く使われるようになりました (文書に画像を挿入する <code>img</code> 要素がその例で、これは最初 NCSA Mosaic に実装されたものです)。いくつかの要素はプロプライエタリなもので、ひとつふたつ程度のブラウザーでしか採用されませんでした。

そのうち、HTML の標準化が求められるようになりました。HTML がどのように表示されるべきかを決定的にまとめた文書 (「仕様」と呼ばれます) があれば、Web ブラウザーを開発する人が HTML を実装するとき、適切に実装されているか確かめることができるからです。

この流れをうけ、[http://www.ietf.org/ IETF (Internet Engineering Task Force)] というインターネットの相互運用性について検討する標準化団体が、HTML 仕様の素案を 1993 年に公開しました。この素案は標準にならず 1994 年に失効してしまいましたが、これが IETF に HTML の標準化を行う作業部会が組織されるきっかけになりました。

1995 年、最初の HTML の草案からアイデアをひろった “HTML 2.0” が策定されました。また、HTML+ という異なる提案も Dave Raggett によって執筆されました。HTML+ は、ブラウザーが実装した新しい要素 (NCSA Mosaic により始まった、画像を挿入する仕組みなど) の多くを基礎とする仕様でした。

同年の後半に、HTML 3.0 の草案が公開されました。しかし、このバージョンはその後の策定が打ち切られました。方向性に関してブラウザーベンダーの指示を取り付けられなかったためです。HTML 3.2 は HTML 3.0 の新機能の多くを廃し、その代わりとして当時人気だった Mosaic や Netscape Navigator というブラウザーが生み出した機能を取り入れることになりました。

1997 年、W3C は HTML 4.0 を勧告として公開しました。このバージョンでは、さらに多くのブラウザー固有の拡張が取り込まれていましたが、それらに理由をつけた上で HTML を整理する試みが行われていました。いくつかの要素を「非推奨」という、現仕様で定義されるが将来的に削除される事を明記したのです。こうすることで、より意味的な HTML の利用を推奨しようとしていました (詳しくは [[The_web_standards_model_-_HTML_CSS_and_JavaScript/ja|Web 標準のモデル]] をご覧ください)。

1999 年には改訂版である HTML 4.01 が公開されました (2001 年に正誤表が更新されています)。これが HTML の最終版になります。しかしながら、現在 HTML 5 の策定が進んでいる最中です。

2000 年に、W3C は XHTML 1.0 仕様を公開しました。これは、HTML を valid な XML 文書フォーマットになるよう再構成したものです。


== HTML 文書の構造 ==
 
シンプルで valid な HTML 文書は、次のようなものになるでしょう。

<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Example page</title>
  </head>
  <body>
    <h1>Hello world</h1>
  </body>
</html></syntaxhighlight>

Web ブラウザーでは以下のように表示されます。

[[File:HTMLrender.png]]

HTML 文書は、「文書型」もしくは「DOCTYPE 宣言」と呼ばれるものから始まります (詳しくは [[Choosing the right doctype for your HTML documents]] をお読みください) 。DOCTYPE 宣言は主に、"標準モード"と呼ばれるものでHTMLを正しくレンダリングするために役立ちます。またバリデーターは、どのHTMLのバージョンでコードを検証するかを知ることができます。現時点では、この意味が分からなくても心配ありません。おいおい解説していきます。この例では、HTML5のDOCTYPE宣言を見ることができます。

DOCTYPE 宣言の次にあるのが、<code>html</code> 要素の開始タグになります。これが、文書全体を囲む要素になります。ですから、<code>html</code> 要素の終了タグは、文書の最後に登場します。<code>html</code>要素は、常に<code>lang</code>属性を持つべきです。これは、ページの主言語を指定します。たとえば、<code>en</code> は"英語"を意味し、<code>fr</code> は"フランス語"を意味します。言語コードを見つけるために、Richard Ishidaの [http://rishida.net/utils/subtags/ Language Subtag Lookup tool] などのツールも使用できます。

<code>html</code> 要素の中には <code>head</code> 要素があります。これは、文書に関する情報 (メタデータ) を格納する部分になります。<code>[[html/elements/head/ja|head]]</code> 要素については 次の記事 でもっと詳しく解説します。<code>head</code> 要素の中にある <code>[[html/elements/title/ja|title]]</code> 要素が、ウインドウに表示されるタイトル (この場合は“サンプルページ”) を指定する要素です。<code>head</code> 要素には常に、ページの文字コードを識別する <code>charset</code> 属性を持つ <code>meta</code> 要素を含める必要があります。可能な限り UTF-8 を使用するべきでしょう。[http://www.w3.org/International/getting-started/characters more about character encodings] も参照してください。

<code>head</code> 要素のあとに <code>[[html/elements/body/ja|body]]</code> 要素が続きます。body 要素はページの内容を囲むもので、この例では “Hello world.” と書かれたひとつの第1レベル見出し ( <code>[[html/elements/hn/ja|h1]]</code> ) が文書の内容になります。

要素は他の要素を含むことが多いです。とくに文書の本文部分は、多くの入れ子になった要素から構成されることでしょう。<code>[[html/elements/article/ja|article]]</code> 、 <code>[[html/elements/header/ja|header]]</code> や <code>[[html/elements/div/ja|div]]</code> 要素などの文書構造要素は、いくつもの区画を構成し、各区画はさらに細分化された区画より構成されます。ここの区画は見出しや段落、リストなどを含むでしょう。段落は、他のページへのリンク、引用、強調などを含むことができます。これらの要素については、後ほど解説していきます。


== HTML 要素の構文 ==


要素は属性を持つことがあります。属性とは要素の挙動を変更したり、意味を付け加えたりするものです。別の例を見てみましょう。
 
<syntaxhighlight lang="html5"><header>
  <h1>The Basics of 
    <abbr title="Hypertext Markup Language">HTML</abbr>
  </h1>
</header></syntaxhighlight>

以下のように表示されます。

[[File:htmlrender2.png]]

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}