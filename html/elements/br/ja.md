{{Page_Title|br}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Modify DOM Interface information.
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|文章をbreakする'''br'''要素はテキストを強制的に終わらせ、brに続くテキストを新たしい行に改めます。}}
{{Markup_Element
|DOM_interface=dom/HTMLBRElement
|Content='''br'''要素は新しい段落を作らずに、強制的に現在のテキスト行を終わらせます。

'''br'''要素は詩や住所など、実際のコンテンツを区切るためだけに使われるべきで、一つの段落で論題のグループを区切るために使うものではありません。その場合は、[[html/elements/p/ja|'''paragraph''']]要素.を使ってください。

'''br'''要素の中にどんなコンテンツ（属性など）を記述しようとも、周囲のテキストの一部とはみなされません。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=以下の例は'''br'''要素の正しい使い方を示しています。
|Code=&lt;p>P. シャーマン&lt;br>
42 ワラビーウェイ&lt;br>
シドニー&lt;/p>
|LiveURL=http://code.webplatform.org/gist/7282007
}}
}}
{{Notes_Section
|Usage='''br'''要素はコンテンツを持たない、タグ１つだけの”置換要素”です。'''class'''などの属性を適用することはできますが、テキストを記述することはできません。

'''br'''は置換要素としてブラウザ側で自動的に閉じられますが、スラッシュを付けて明示的に閉じることもできます。
|Notes=閉じタグは不要です。
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-br-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-br-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-BR
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
}}
{{Topics|HTML, XHTML}}
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