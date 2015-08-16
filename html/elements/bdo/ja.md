{{Page_Title|bdo}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|'''bdo'''要素はページ上のテキスト表記の方向を定義することができます。（”BDO”とはBi-Directional Override（双方向オーバーライド）の略です。）}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=inline
|Content=<code>bdo</code>に関連する国際化トピック:
* [http://www.w3.org/International/techniques/authoring-html#bdo Overriding the Unicode bidirectional algorithm]
* [http://www.w3.org/International/techniques/authoring-html#inline Mixing text direction inline]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=
この例ではテキストを正しく読める向きに表示するために'''bdo'''要素を使っています。正しく読める順番で書いたテキストを[[html/attributes/dir/ja|'''dir''']]属性に'''ltr'''を指定した'''bdo'''タグの間に記述することで双方向アルゴリズムを無効化することができます。

以下のテキストには英語のように左から右に書いた文字列とヘブライ語のように右から左に書いた文字列が含まれています。この文は英語です、すで語イラブヘは文のこ。

この右から左に書かれたテキスト（すで語イラブヘは文のこ。）はすでにひっくり返っているようにに思えますが、画面上では正しい向きで表示されます。その後Unicodeの双方向アルゴリズムが適用される場合、テキストは2回ひっくり返されて右から左ではなく左から右に、正しくないない表示になってしまいます。
|Code=&lt;BDO DIR{{=}}"ltr"&gt;この文は英語です、
    すで語イラブヘは文のこ。&lt;/BDO&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====備考===
'''bdo'''要素はテキストの表示方向を制御することができ、Unicodeの双方向アルゴリズムでは文字列に埋め込まれた方向にテキストを自動的に変換します。

例えば、英語文書は基本的に左から右(ltr)に書かれます。
しかし、右から左(rtl)に書かれる言語を含む一部の文節がドキュメント内にある場合、双方向アルゴリズムを用いて方向を変換しなければいけません。
通常埋め込まれた方向を変えるのには双方向アルゴリズムと[[html/attributes/dir|'''dir''']]属性で十分です。
しかし双方向アルゴリズムで、フォーマットされたテキストを表示しようとしても、正しく表示されない場合があります。
例えば、英語とヘブライ語を含む段落で正しく逆方向にされていないメールアドレスなどがある場合などです。
これはヘブライ語の方向がメールアドレスまでも逆にし、双方向アルゴリズムによって2回逆にされてしまったためです。

bdo要素はアルゴリズムを無効化し、表示順を制御します。
bdo要素を使う上で[[html/attributes/dir|'''dir''']]属性は必須です。
bdo要素はInternet Explorer 5以上で利用可能です。
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-bdo-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-bdo-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/dirlang.html#edef-BDO
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/properties/direction|direction]]</code>
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}