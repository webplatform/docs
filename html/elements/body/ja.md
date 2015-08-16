{{Page_Title|body}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Data Not Semantic, Unreviewed Import
|Content=Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|'''body'''要素はドキュメントの主要コンテンツを表します。}}
{{Markup_Element
|DOM_interface=dom/HTMLBodyElement
|Tag_omissions=Start and end are omissible in some cases
|CSS_display=block
|Content=<code><body></code>要素はスクリプトからアクセスすることができます。

<body>要素を持つウィンドウオブジェクトは<code>onblur</code>、<code>onfocus</code>、<code>onload</code>、<code>onunload</code>イベントをハンドリングすることができます。

=== HTMLイベントハンドラコンテンツ属性===

{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}<code>onafterprint</code> 
{{!}}ユーザが現在のドキュメントを印刷
{{!}}-
{{!}}<code>onbeforeprint</code> 
{{!}}ユーザが現在のドキュメントの印刷をリクエスト
{{!}}-
{{!}}<code>onbeforeunload</code> 
{{!}}ドキュメントがunloadされようとしている
{{!}}-
{{!}}<code>onblur</code> 
{{!}}ドキュメントからフォーカスが外れた
{{!}}-
{{!}}<code>onerror</code> 
{{!}}ドキュメントがプロパティの読み込みに失敗
{{!}}-
{{!}}<code>onfocus</code> 
{{!}}ドキュメントがフォーカスされた
{{!}}-
{{!}}<code>onhashchange</code> 
{{!}}ドキュメントの現在のアドレスのフラグメント識別子が変更された
{{!}}-
{{!}}<code>onload</code> 
{{!}}ドキュメントのロードが完了
{{!}}-
{{!}}<code>onmessage</code> 
{{!}}ドキュメントがメッセージを受信
{{!}}-
{{!}}<code>onoffline</code> 
{{!}}ネットワークのコネクションが失敗
{{!}}-
{{!}}<code>ononline</code> 
{{!}}ネットワークのコネクションが復帰
{{!}}-
{{!}}<code>onpopstate</code> 
{{!}}ユーザがセッションヒストリーを遷移
{{!}}-
{{!}}<code>onredo</code> 
{{!}}ユーザがトランザクション履歴をやり直した
{{!}}-
{{!}}<code>onresize</code> 
{{!}}ドキュメントのビューがリサイズされた
{{!}}-
{{!}}<code>onstorage</code> 
{{!}}ドキュメントのビューがリサイズされた
{{!}}-
{{!}}<code>onundo</code> 
{{!}}ユーザがトランザクション履歴を取り消した
{{!}}-
{{!}}<code>onunload</code> 
{{!}}現在のドキュメントから移動
{{!}}}

以下の属性は、もう使われておらず、今後は使うべきではありません。

<code>alink</code>, <code>bgcolor</code>, <code>link</code>, <code>marginbottom</code>, <code>marginheight</code>, <code>marginleft</code>, <code>marginright</code>, <code>margintop</code>, <code>marginwidth</code>, <code>text</code>, <code>vlink</code>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=<code><body></code>要素が<code><head></code>に続き、全体が<code><html></code>要素に含まれています。
|Code=<syntaxhighlight lang="html5">
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>The HTML Document</title>
</head>
<body>
<p>The HTML content</p>
</body>
</html>
</syntaxhighlight>
|LiveURL=http://test.w3.org/html/examples/elements/body/body01.html
}}{{Single Example
|Language=JavaScript
|Description=この例では、javascriptで<code><body></code>を取得します。
|Code=<syntaxhighlight lang="javascript">var oBody = document.body;</syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/sections.html#the-body-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/sections.html#the-body-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-BODY
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
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
|Browser=Internet Explorer (Windows)
|Version=8+
|Note=The value of the <code>background</code> attribute depends on the current document compatibility mode.
}}{{Compatibility Notes Row
|Browser=Internet Explorer (Windows)
|Version=6
|Note=When you use the <code>!DOCTYPE</code> declaration to specify standards-compliant mode, this object no longer represents the entire surface onto which a document's contents can be rendered. The object can obtain its size from its content, or you can set its size explicitly like a <code>div</code> object.
}}{{Compatibility Notes Row
|Browser=Internet Explorer (Windows)
|Version=6+
|Note=As of Microsoft Internet Explorer 6, when you use the <code>!DOCTYPE</code> declaration to specify standards-compliant mode, the <code><body></code> object can obtain its size from its content, or you can set its size explicitly—like a <code>div</code> object, for example. In standards-compliant mode, the <code><html></code> element represents the entire surface onto which a document's contents can be rendered. When the <code>!DOCTYPE</code> declaration does not specify standards-compliant mode, and with earlier versions of Windows Internet Explorer, the <code><body></code> object represents the entire surface onto which a document's contents can be rendered. The size of the <code><body></code> object cannot be changed and is equal to the size of the window. Margins you set on this object are rendered inside the border and scrollbars of the object.
}}
}}