{{Page_Title|address}}
{{Flags
|State=Not Ready
|Editorial notes=Add syntax, attribute, example, compatibility.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|'''<address>'''は文書や記事の所有者・著者とコンタクトをとるための情報を囲む要素です。}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=* <address>要素は、addressと言っても住所情報を記載するためものではありません。（実際に関連する住所情報の場合は別ですが）
* <address>には連絡を取るための情報以外の情報を記載してはいけません。
* 一般的に、<address>要素は<footer>要素の中で、他の情報の間に記載します。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=W3Cのサイトでは以下の様な連絡先情報を記載しています。
|Code=&lt;address>
    &lt;p>&lt;a href="http://www.w3.org/Consortium/contact-mit">MIT&lt;/a>&lt;/p>
&lt;/address>
}}{{Single Example
|Description=<address>要素の中に以下のような情報（最終更新日時など）を入れるのは正しくありません。
|Code=&lt;div>Last Modified: 1999/12/24 23:37:50&lt;/div>
}}
}}
{{Notes_Section
|Notes=WebKit（safariや古いAndroid系）やTrident（Internet Explorer）では以下のようにデフォルトでスタイルが設定されています。
<pre>address {
	display:block;
	font-style: italic;
}</pre>
Gecko(Firefox)では以下のように設定されています。
<pre>address, address[dir]{
         unicode-bidi: -moz-isolate;
         display:block;
         font-style:italic;
}</pre>
|Import_Notes====標準情報===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 7.5.6


===HTML情報===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
{{!}}-
!CSS Display
{{!}}block
{{!}}}

 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/sections.html#the-address-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/sections.html#the-address-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-ADDRESS
|Status=W3C Recommendation
}}
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{Languages}}