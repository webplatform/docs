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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}