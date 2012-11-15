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