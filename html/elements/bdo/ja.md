{{Page_Title|bdo}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|'''bdo'''要素によって、ページ上のテキスト表記の方向を指定できます。（”BDO”とはBi-Directional Override（双方向オーバーライド）の略です。）}}
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
|Description=この例では、'''bdo'''要素を使って、テキストを読む向きを変更しています。

以下のテキストには、日本語のように左から右に書く文字列と、ヘブライ語のように右から左に書く文字列が含まれています。例：この文は日本語です、すで語イラブヘは文のこ。

「すで語イラブヘは文のこ」はいま逆順に入力されていますが、ヘブライ語として正しい向きの表示を模擬していると仮定してください。この文章に対して、Unicodeの双方向アルゴリズムを適用すると、テキストはもう一度ひっくり返されて、右から左に進むべきところが左から右に、誤った方向で表示されてしまいます。
|Code=&lt;BDO DIR{{=}}"ltr"&gt;この文は日本語です、
    すで語イラブヘは文のこ。&lt;/BDO&gt;
}}
}}
{{Notes_Section
|Notes====備考===
'''bdo'''要素によって、テキストの表示方向を制御できます。Unicodeの双方向アルゴリズムは自動的に、文字列にもともと埋め込まれている方向を見て処理します。例えば、日本語の基本の方向は左から右(ltr)です。
その中に、右から左(rtl)に書かれる言語を含む文節がある場合、双方向アルゴリズムが用いられて方向が変換されます。
通常は、双方向アルゴリズムおよび[[html/attributes/dir|'''dir''']]属性だけあれば、埋め込まれた方向の変更を解釈するのに十分です。
しかし、フォーマットされたテキストに双方向アルゴリズムがかけられて表示されるときは、正しく表示されない場合があります。
例えば、日本語とヘブライ語を含むメールのフォーマットで、誤った方向にされてしまう場合などです。
これは、メールのフォーマットが双方向アルゴリズムに一度通されていて、もう一度双方向アルゴリズムにかけるとヘブライ語の単語の進行方向がもう一度逆にされるためです。

bdo要素は双方向アルゴリズムを無効化し、表示順を強制します。
bdo要素を使う場合、[[html/attributes/dir|'''dir''']]属性が必須です。
bdo要素はInternet Explorer 5以上で利用可能です。
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-bdo-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-bdo-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/dirlang.html#edef-BDO
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[css/properties/direction|direction]]</code>
}}
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