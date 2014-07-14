{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>text-justify</code> CSS property offers a fine level of justification control over the enclosed content, allowing for a variety of sophisticated justification models used in different language writing systems.}}
{{CSS Property
|Initial value=auto
|Applies to=block containers and, optionally, inline elements
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=textJustify
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Allows the browser to determine which justification algorithm to apply.
}}{{CSS Property Value
|Data Type=none
|Description=Justification is disabled.
}}{{CSS Property Value
|Data Type=inter-word
|Description=Aligns text by increasing the space between words. This value's spacing behavior is the fastest way to make all lines of text equal in length. Its justification behavior does not affect the last line of the paragraph. This value is typically used for languages that separate words using spaces, like English or Korean.
}}{{CSS Property Value
|Data Type=inter-ideograph
|Description=Justifies lines of ideographic text, and increases or decreases both inter-ideograph and inter-word spacing. This value is typically used for CJK languages.
}}{{CSS Property Value
|Data Type=inter-cluster
|Description=Justifies lines of text that contain no inter-word spacing. This value is typically used for Southeast Asian scripts such as Thai.
}}{{CSS Property Value
|Data Type=distribute
|Description=Aligns text by increasing the space between both of words and characters. This value is sometimes used in e.g. Japanese.
}}{{CSS Property Value
|Data Type=kashida
|Description=Justifies lines of text by elongating characters at chosen points.  This form of justification is intended for Arabic script languages.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The first paragraph is using <code>inter-word</code> as a value of text-justify property, in English. The second one is using <code>distribute</code> in Japanese paragraph.
|Code=&lt;p class="english"&gt;This is a simple paragraph with a altered text-justify value by inter-word.&lt;/p&gt;

&lt;p class="japanese"&gt;日本語では、どのように表示されるかを見てみましょう。日本語の場合にはdistributeが使用される場合があります。&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5671702
}}{{Single Example
|Language=CSS
|Code=p {
	width: 300px;
	text-align: justify;
	text-align-last: justify;
}

p.english {
    text-justify: inter-word;
}

p.japanese {
	text-justify: distribute;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#text-justify0
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.0 +
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=8.0 +
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Manual_sections=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}