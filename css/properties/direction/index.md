{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>direction</code> CSS property specifies the text direction/writing direction. The <code>rtl</code> is used for Hebrew or Arabic text, the <code>ltr</code> is for other languages.}}
{{CSS Property
|Initial value=ltr
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=direction
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=ltr
|Description=Default. Content flows left to right.
}}{{CSS Property Value
|Data Type=rtl
|Description=Content flows right to left.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example demonstrates how to set and retrieve the value of the '''direction''' property.
|Code=&lt;p&gt;This is a paragraph using default writting direction(ltr).&lt;/p&gt;

&lt;p class="rtl"&gt;This is a paragraph using right-to-left direction.&lt;/p&gt;

&lt;p class="rtl" id="bidi"&gt;The paragraph using rtl and sets the bidi-override as value of unicode-bidi property.&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5708516
}}{{Single Example
|Language=CSS
|Code=p {
	width: 300px;
	background-color: #cccccc;
}

.rtl {
	direction: rtl;
}

#bidi {
	unicode-bidi: bidi-override;
}
}}
}}
{{Notes_Section
|Notes=The property does not affect alphanumeric characters in Latin documents. These characters always render '''ltr'''.  However, the property does affect punctuation characters in Latin documents.
The property pertains only to the directional flow of an element's content. It has no effect on properties such as [[css/properties/left|'''left''']] or [[css/properties/right|'''right''']], [[css/properties/margin-left|'''margin-left''']] or [[css/properties/margin-right|'''margin-right''']].  The '''margin-left''' property, for example, sets or retrieves the width of the margin on the left side of the document regardless of the value of the '''direction''' property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Cascading Style Sheets Level 2 Revision 1
|URL=http://www.w3.org/TR/CSS2/visuren.html#propdef-direction
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[html/attributes/dir|dir]]</code>
*<code>Conceptual</code>
*<code>HTML Character Sets</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}