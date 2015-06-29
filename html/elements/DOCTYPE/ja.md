{{Page_Title|!DOCTYPE}}
{{Flags
|State=In Progress
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|'''文書型宣言（DOCTYPE宣言）'''とはSGMLやXML文書を文書型定義(DTD)（HTMLのバージョンごとの書式の定義など）と結びつけるためのものです。シリアライズされたフォームの中では、特定の構文に準拠したマークアップの短い文字列として現れます。<!DOCTYPE> を書かないとQuirksモード(互換モード)で表示されます。
{{Languages}}}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=HTML5ではDOCTYPE宣言は以下のように記述されます。
|Code=<!DOCTYPE html>
}}{{Single Example
|Language=HTML
|Description=HTML4.01のStrict DTDでは
|Code=<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
}}{{Single Example
|Language=HTML
|Description=HTML4.01のTransitional DTDでは
|Code=<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
}}
と記述されます。
}}
{{Notes_Section
|Usage=htmlファイルの始まりの部分に <syntaxhighlight lang="HTML5">
<!DOCTYPE html>
</syntaxhighlight> を追加してください。
|Notes=<!DOCTYPE>はHTML文書の<html>タグより前の一番最初の部分に書かなければいけません。

<!DOCTYPE>はHTMLのタグではなく、ブラウザにそのhtmlファイルのバージョン情報を教えるためのものです。

HTML4.01はSGMLベースであり、<!DOCTYPE>では参照するDTDを指定します。
DTDがマークアップ言語用のルールを定義しているため、ブラウザはコンテンツを正しく表示することができます。

一方HTML5はSGMLベースではないため、DTDを参照する必要がありません。
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Deprecated, HTML
|Manual_links=html/quirksmode
}}
{{Topics|DOCTYPE, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}