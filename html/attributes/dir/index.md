{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Global attribute. Specifies the element’s text directionality.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=dir = "ltr" or "rtl" or "auto"
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=For pages in Arabic, Hebrew, Persian, Thaana, Urdu, etc. set the default direction of the page to right-to-left by including dir in the html tag.
|Code=<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
...
}}{{Single Example
|Language=HTML
|Description=To make the exclamation mark appear to the left of the citation, surround the citation with markup and add a dir attribute.
|Code=&lt;p&gt;The title is &quot;&lt;span dir=&quot;rtl&quot; lang=&quot;ar&quot; xml:lang=&quot;ar&quot;&gt;مفتاح معايير الويب!&lt;/span&gt;&quot; in Arabic.&lt;/p&gt;
|LiveURL=http://www.w3.org/International/php/examples/generate?data=bidi&test=18
}}
}}
{{Notes_Section
|Notes====Remarks===
Unless explicitly set, the '''dir''' property has no return value when accessed in script.
The property does not affect alphanumeric characters in Latin documents. These characters always render '''ltr'''.  However, the property does affect punctuation characters in Latin documents. For example, punctuation marks such as periods and question marks render to the left of a sentence when the [[dom/properties/dir (Document object)|'''dir''']] property is set to '''rtl'''. The real benefit of this attribute is when using '''rtl''' languages such as Arabic and Hebrew. These can be some of the most challenging languages to write '''HTML''' with especially because html in itself is a left-to-right programming language.

For more information see the following links:
* [http://www.w3.org/International/techniques/authoring-html#direction Text direction]
* [http://www.w3.org/International/techniques/authoring-html#using Setting up a right-to-left page ]
* [http://www.w3.org/International/techniques/authoring-html#blocks Setting direction on block elements]
* [http://www.w3.org/International/techniques/authoring-html#inline Mixing text direction inline]
* [http://www.w3.org/International/techniques/authoring-html#mirrored Handling parentheses and other mirrored characters]
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>area</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>hn</code>
*<code>html</code>
*<code>i</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>optGroup</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[css/properties/direction|direction]]</code>
*<code>Conceptual</code>
*<code>HTML Character Sets</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}