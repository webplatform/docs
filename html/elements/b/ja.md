{{Page_Title|b}}
{{Flags
|State=In Progress
|Editorial notes=Add compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|'''&lt;b>'''要素は特に重要であることを伝えるのに使うものではなく、あくまで通常の文章において文体的にテキストを強調する際に使用します。}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=
|CSS_display=
|Content=&lt;b>要素は通常、ブラウザ上でテキストを太字で表示するのに使われます。多くのブラウザで広くサポートされていますが、CSSでより意味的に適切な要素で全く同じ効果を表現できるため、太字にするという目的のために'''&lt;b>'''要素を使用するのは推奨されていません。HTML5では、'''&lt;b>'''要素の意味が再定義され、他のテキストと区別するために使われるようになりました。周囲のテキストよりも重要であるという意味はもうありません。

&lt;b>要素は他に適切な要素がない場合の最終手段として使うようにしてください。そのテキストがスタイル的に重要だと示されている以外の意味はありません（[[html/elements/span/ja|'''span''' 要素]]の省略形とい言ってもいいでしょう）。意味があり、似たような効果をもたらす要素として、[[html/elements/strong/ja|strong]]、[[html/elements/dfn/ja|dfn]]、[[html/elements/hn/ja|h1-h6]]、[[html/elements/abbr/ja|abbr]].があります。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=以下の例では、アドベンチャーゲームのテキストの特別な部分を'''&lt;b>'''要素を使って強調しています。
|Code=&lt;p>あなたは小さな部屋に入りました。
するとあなたの&lt;b>剣&lt;/b>が眩しく輝き始めました。
&lt;b>ネズミ&lt;/b>は壁の隅をちょこまかと走って行きました。&lt;/p>
|LiveURL=http://code.webplatform.org/gist/7281844
}}{{Single Example
|Language=HTML
|Description=こちらの例では、'''&lt;b>'''要素を使って社名と製品名を強調しています。CSSの曖昧さ回避のため、'''class'''属性を使用しています。
|Code=&lt;p>&lt;b class="org">Acme &lt;abbr title="Corporation">Corp&lt;/abbr>&lt;/b>は&lt;b class="product">ウィジェットブラスト3000&lt;/b>を紹介することができ、とても嬉しく思っています。
これは朝卵を焼くところから夜子供を寝かしつけるまで、あなたの生活を楽にする現代科学の奇跡です。&lt;/p>
|LiveURL=http://code.webplatform.org/gist/321e5149c1e661e1de14
}}
}}
{{Notes_Section
|Usage='''&lt;b>'''要素は人名、社名、製品名、地名などの固有名詞を囲んで、周囲のテキストと区別するために使いますが、意味という意味はありません。

'''&lt;b>'''要素に関連する国際化トピック

* [[http://www.w3.org/International/techniques/authoring-html#bandi|Using b and i tags]]
|Notes='''&lt;b>'''要素は意味を持たないため、自分で意味を持たせて使ってはいけません。もっと適切な要素があるはずです。見出しには'''&lt;h1>'''～'''&lt;h6>'''要素を、アクセントを付けたい場合は'''&lt;em>'''要素を、重要性を示すには'''&lt;strong>'''要素を、文脈上重要/強調したいテキストには'''&lt;mark>'''要素を使うべきでしょう。
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-b-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-b-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/present/graphics.html#edef-B
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
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
|Mobile_rows=
|Notes_rows=
}}
{{Languages}}