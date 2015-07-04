{{Page_Title|a}}
{{Flags
|State=In Progress
|Editorial notes=Add more example
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|<a>タグはハイパーリンクやリンク先を定義します。}}
{{Markup_Element
|DOM_interface=dom/HTMLAnchorElement
|Tag_omissions=required
|CSS_display=inline
|Content====概要===

<code>&lt;a></code>要素は外部サイトや、内部の別ページ・別セクション、画像やローカルファイルへのハイパーリンクを定義します。

===構文===

<pre><a href="[URI]">[アンカーテキストまたはイメージタグ]</a></pre>
<pre><a id="#[ID]">[アンカーテキストまたはイメージタグ]</a></pre>
<pre><a><a>[アンカーテキストまたはイメージタグ]</a></a></pre>

===<a><a>タグで囲まれたHTMLL===

一般的にはテキストか画像を<code>&lt;a>&lt;/a></code> タグで囲みます。
囲まれたHTMLはページ内に表示され、[[html/attributes/href/ja|href]]属性を指定していた場合はリンクとして描画されます。


===一般的な属性===

{{{!}} class="wikitable"
! 名前
! 値
! 目的
! 例
! 有効
{{!}}-
{{!}} [[html/attributes/download/ja|'''download''']]
{{!}} テキスト
{{!}} 保存ダイアログに表示するファイル名を指定することができます
{{!}} <pre>download="filename.pdf"</pre>
{{!}} HTML5
{{!}}-
{{!}} [[html/attributes/href/ja|'''href''']]
{{!}} [http://www.w3.org/Addressing/URL/uri-spec.html URI]
{{!}} 対象のリンクを指定します
{{!}} <pre>href="http://example.com"</pre> <pre>href="#TableOfContents"</pre>
{{!}} &nbsp;
{{!}}-
{{!}} [[html/attributes/id/ja|'''id''']]
{{!}} 識別用のテキスト
{{!}} hrefで参照するためのアンカーを生成します
{{!}} <pre>id="TableOfContents"</pre>
{{!}} &nbsp;
{{!}}-
{{!}} [[html/attributes/hreflang/ja|'''hreflang''']]
{{!}} [http://www.ietf.org/rfc/bcp/bcp47.txt HTML5] または [http://www.ietf.org/rfc/rfc1766.txt HTML4]用の言語タグ
{{!}} リンク先の言語のヒントです。 リンク元からリンク先へのヒントとしてrel="alternate"とともに記述して使用できます。
{{!}} <pre>hreflang="ja"</pre>
{{!}}-
{{!}} [[html/attributes/rel/ja|'''rel''']]
{{!}} カンマ区切りのキーワードリスト
{{!}} 現在のページとリンク先の関係を示します
{{!}} <pre>rel="help"</pre>
{{!}} &nbsp;
{{!}}-
{{!}} [[html/attributes/target/ja|'''target''']]
{{!}} [http://www.w3.org/TR/html5/browsers.html#valid-browsing-context-name-or-keyword ブラウジング・コンテキスト]
{{!}} リンクをどこで開くか指定できます
{{!}} <pre>target="_blank"</pre>
{{!}} &nbsp;
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!-- 外部サイトへのリンク -->
<a href="http://www.example.com">ウェブサイト</a>

&lt;!-- 同一ディレクトリの内部サイトへのリンク --&gt;
<a href="home.html">ホーム</a>

&lt;!-- ダウンロードリンク (HTML5のみ)。 download属性には保存ダイアログに予め設定するファイル名を指定します。
    download属性に値を設定しない場合、リソース名が設定されます。-->
<a href="filename_on_server.pdf" download="meaningful_filename.pdf">pdfファイルをダウンロード</a>

&lt;!-- target属性で指定したウィンドウでリンクを開きます。 -->
<a href="http://www.example.com" target="_blank">新しいウィンドウでウェブサイトを開</a>

&lt;!-- リンクの一部分としてimg要素を導入します --&gt;
<a href{{=}}"http://www.example.com"><img src="images/bullet.png">画像リンク</a>

&lt;!-- ページ内のアンカーへのリンク -->
<a href="#top">トップへ</a>

&lt;!-- アンカーを定義します。 -->
<a id="top"></a>

&lt;!-- javascriptの関数を呼び出す (推奨されません) -->
<a href="javascript:alert('リンクがクリックされました')">リンクをクリックしてください</a>

&lt;!-- ドキュメントへのリンクとリンク先のドキュメントとの関係をrel属性で指定します。 -->
<a href="http://www.example.com/help" rel="help">ヘルプへ</a>
|LiveURL=http://code.webplatform.org/gist/5281100
}}
}}
{{Notes_Section
|Notes====備考===
ページ内にアンカーを作成する際、[[html/attributes/name/ja|'''name''']] 属性はもはや誰も使っていません。[[html/attributes/id/ja|'''id''']]で置き換えるべきでしょう。

テキストも画像もアンカーに指定することができます。アンカーとなった画像はフチに訪問済みかどうかを示す色がつくようになります。このフチの色を表示させないためには、"img"要素の[[html/attributes/border/ja|'''border''']]属性に0を設定するか、'''border'''属性を省略する必要があります。CSS属性を使用することで、'''a'''要素と'''img'''要素のデフォルトの見た目を上書くことができます。

URIはhttpやmailto、fileなどのプロトコルを指定します。
フラグメント（#に続くテキスト）を指定することで現在のページの特定の位置へジャンプできます。hrefはメニューの中の現在のページを参照するような狩りのリンクを省略することができます。

また、任意ですが、[[html/attributes/rel/ja|'''rel''']]属性で対象のリンクにセマンティックな意味を付与することができます。

<code>a</code>要素に関連する国際化トピック：
* [http://www.w3.org/International/techniques/authoring-html#linkdestination Indicating the language of a link destination]

===クリックとフォーカス===
ブラウザ/OS別　アンカーをクリックした際、自動でフォーカスが切り替わるか

アンカーをクリックしたときフォーカスされるか？
{{{!}} class="wikitable"
{{!}}--
!Desktop Browsers
{{!}}Windows 8.1
{{!}}OS X 10.9
{{!}}--
!Firefox 30.0
{{!}}Yes
{{!}}Yes
{{!}}-
!Chrome [https://code.google.com/p/chromium/issues/detail?id=388666 >=39]
{{!}}Yes
{{!}}Yes
{{!}}-
!Safari 7.0.5
{{!}}N/A
{{!}}[[html/attributes/tabIndex/ja|<code>tabindex</code>]]のみ
{{!}}-
!Internet Explorer 11
{{!}}Yes
{{!}}N/A
{{!}}-
!Presto (Opera 12)
{{!}}Yes
{{!}}???
{{!}}}

アンカーをタップしたときフォーカスされるか？
{{{!}} class="wikitable"
!Mobile Browsers
{{!}}iOS 7.1.2
{{!}}Android 4.4.4
{{!}}-
!Safari Mobile
{{!}}[[html/attributes/tabIndex/ja|<code>tabindex</code>]]のみ
{{!}}N/A
{{!}}-
!Chrome 35
{{!}}???
{{!}}[[html/attributes/tabIndex/ja|<code>tabindex</code>]]のみ
{{!}}}
|Import_Notes= 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-a-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-a-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/links.html#edef-A
|Status=W3C Recommendation
}}
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{Feature=a}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/a
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and later
|Note=A [[html/elements/table|'''table''']] object does not function properly when contained within an '''a''' tag. The value of the [[html/attributes/href|'''href''']] attribute depends on the current document compatibility mode.  Internet Explorer 8 and later. When Protected Mode is enabled and a Web page contains an '''anchor link''' with a named [[html/attributes/target|'''target''']], Windows Internet Explorer opens the target of the link in a new window when the target has a different integrity level than the Web page containing the link. For more information, see Understanding and Working in Protected Mode Internet Explorer.
}}{{Compatibility Notes Row
|Browser=Safari / Google Chrome
|Version=any
|Note=<code>A</code> elements with href don't get focus by mouse press by default.
}}
}}