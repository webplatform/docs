{{Page_Title|article}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|'''&lt;article&gt;'''はページ内で単独で完結する構成要素を定義します。}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=required
|CSS_display=block
|Content=<article>は&lt;div&gt;タグを減らすためにHTML5から導入された要素です。'''<article>'''は主に以下の内容を表します。

* フォーラムの投稿
* 雑誌や新聞の記事
* ブログのエントリ
* ユーザの投稿したコメント
* インタラクティブなウィジェット/ガジェット

上記以外にも独立したコンテンツを表すのに使います。

'''<article>'''要素をネストする時は、内側の<article>の内容は外側の<article>に関連したコンテンツでなければいけません。例えば、コメントの付いたブログのエントリでは、ブログエントリの'''<article>'''の中にコメントの'''<article>'''をネストするほうがよいでしょう。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=以下の例では'''<article>'''、'''<header>'''、'''<footer>'''を使った記事の基本構成を示します。
|Code=&lt;article&gt;
 &lt;header&gt;
  &lt;h1&gt;見出し&lt;/h1&gt;
 &lt;/header&gt;
 &lt;p&gt;本文&lt;/p&gt;
 &lt;p&gt;...&lt;/p&gt;
 &lt;footer&gt;フッター&lt;/footer&gt;
&lt;/article&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/sections.html#the-article-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/sections.html#the-article-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=[[html/elements/nav/ja|nav]] - <article>タグの子要素としてよく用いられます。
|External_links=* http://www.w3.org/TR/html-markup/article.html#article
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=21
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=14
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.5
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9
|Note=The '''article''' element is only supported for webpages displayed in IE9 Standards mode. Internet Explorer 9 does not natively support the '''time''' element, which is intended to provide the publication date of the article element.
}}
}}