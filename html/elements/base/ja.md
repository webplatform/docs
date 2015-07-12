{{Page_Title|base}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|'''&lt;base>'''は文書の基準となるURLを明示し、文書内の相対URLを解決するために使用します。.}}
{{Markup_Element
|DOM_interface=dom/HTMLBaseElement
|Tag_omissions=No end tag (self-closing)
|CSS_display=none
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px"><em>なし</em></td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>[[html/elements/head|<code>&lt;head&gt;</code>]]タグ内で1度のみ許可されています。</td>
</tr>
</table>

アクセスする前に相対URL（<var>some/example.html</var>）を絶対URL(<var>http://example.org/some/example.html</var>) に変換しなければいけません。通常、相対URLを解決するためのベースURLとしてそのドキュメントのURL（JavaScriptで使用する[[dom/Location/ja|<code>location</code>]]オブジェクト）が使用されます。&lt;base>要素の[[html/attributes/href/ja|<code>href</code>]]属性を記述することでデフォルトのベースURLを上書く事ができます。

リンク([[html/elements/a/ja|<code>&lt;a&gt;</code>]])やフォーム([[html/elements/form/ja|<code>&lt;form&gt;</code>]])で[[html/attributes/target/ja|<code>target</code>]]を開きますが、デフォルトのtargetは<var>_self</var>で、現在ドキュメントを表示しているのと同じウィンドウでリンクを開くことになります。<code>&lt;base target="…"&gt;</code>と書くことでドキュメント全体のtargetのデフォルトを上書くことができます。

ドキュメントが[[html/elements/iframe/ja|<code>iframe</code>]]を使って構成されている場合、<code>&lt;base target="_parent"&gt;</code>と設定することで親フレームでリンクを開くことができます。フレームを使っていないドキュメントで<var>_parent</var>や<var>_top</var>を使用する場合、<var>_self</var>と同じ動きになります。



== HTML属性==

*<code>href</code>= URI（前後のスペースは取り除かれます。）<br />href属性を指定した<base>要素は、URLを使う属性を持つ他の要素よりも前に記述しなければいけません。（<html>要素以外。manifest属性はbase要素の影響を受けないため。）[[#Example_A|[Example A]]]

*<code>target</code> = ブラウジング・コンテキストの名前、もしくは_blank, _self, _parent, _topのいずれか<br />ハイパーリンクやフォームがナビゲーションを表している場合、base要素のtarget属性の値がデフォルト値になります。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=この例は関連ドキュメント<var>some-file.html</var>へのリンクを<var>http://example.org/deep/some-file.html</var>に書き換えています。
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;base要素の例&lt;/title&gt;
    &lt;base href="http://www.example.org/deep/"&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;p&gt;&lt;a href="some-file.html"&gt;関連リンク&lt;/a&gt;&lt;/p&gt;
    &lt;!-- 上記のリンクを解決すると下記のようになります --&gt;
    &lt;p&gt;&lt;a href="http://www.example.org/deep/some-file.html"&gt;関連リンク&lt;/a&gt;&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=HTML
|Description=こちらの例では'''base'''要素より下に書かれている要素のみが影響を受けています。
|Code=&lt;head&gt;
  &lt;title&gt;base要素の例&lt;/title&gt;
  &lt;link href="my-style.css&quot; rel="stylesheet"&gt;
  &lt;base href="http://example.com"&gt;
  &lt;link href="my-other-style.css" rel="stylesheet"&gt;
  &lt;!--
    [current domain and directory]/my-style.css
    http://example.com/my-other-style.css
    のように解釈されます。
  --&gt;
&lt;/head&gt;
}}{{Single Example
|Language=HTML
|Description=こちらの例では複数の'''base'''要素を記述していますが、無視されています。
|Code=&lt;head&gt;
  &lt;title&gt;base要素の例&lt;/title&gt;
  &lt;base href="http://example.com"&gt;
  &lt;base target="_blank"&gt;
  &lt;base href="http://webplatform.org" target="_top"&gt;
  &lt;!--
    base要素の定義は1つにまとめられます：
    &lt;base href="http://example.com/" target="_blank"&gt;
    例外として、Internet Explorerでは最初の要素のみが有効になります：
    &lt;base href="http://example.com/" target="_self"&gt;    
  --&gt;
&lt;/head&gt;
}}
}}
{{Notes_Section
|Notes=* Firefox 4とInternet Explorer 10は<code>&lt;base&gt;</code>要素に相対URLを指定することができます。これにより相対URLで相対URLを解釈することができます<br/>（訳注:その他のブラウザも対応しているようです）。
* <code>&lt;base&gt;</code>はそれよりも下で記述した要素に対してのみ有効です。
* 複数の<code>&lt;base&gt;</code>を宣言するのは不正で、それぞれ最初の[[html/attributes/href/ja|<code>href</code>]]と[[html/attributes/target/ja|<code>target</code>]]のみが使用され、残りは破棄されます。Internet Explorer一番最初に書かれた<code>&lt;base&gt;</code>しか読んでくれません。

'''注''' インラインSVGで使われる<code>fill="url(#element-id)"</code>のような参照は<code>&lt;base&gt;</code>を使ったドキュメントでは問題になります。<code>url(#element-id)</code>で正しいURLが取得されますが、CSS セレクターでは正しく認識されません。
最新のFirefox とChrome ではその影響を非常に受けやすくなっています。
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/document-metadata.html#the-base-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/document-metadata.html#the-base-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/links.html#edef-BASE
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/base Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535191%28v=vs.85%29.aspx Microsoft Developer Network]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{Languages}}