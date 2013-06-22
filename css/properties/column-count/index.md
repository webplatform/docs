{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the number of columns an element should be divided into.}}
{{CSS Property
|Initial value=auto
|Applies to=non-replaced block-level elements (except table elements), table cells, and inline-block elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=columnCount
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=count
|Description=An integer value that specifies the number of columns in the multi-column element. Values must be greater than 0. When [[css/properties/column-width|'''column-width''']] is specified with [[css/properties/column-count|'''column-count''']] and both have non-auto values, the integer value defines the maximum number of columns.
}}{{CSS Property Value
|Data Type=auto
|Description=The number of columns is determined by the values of other property values of the multi-column element, such as [[css/properties/column-width|'''columnWidth''']].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=This example shows how to render text within the section.newspaper element in three columns.
|Code=div {
  column-count: 3;
}
}}{{Single Example
|Language=CSS
|Description=We will always display 3 columns adjusting the width of the columns as needed
|Code=/* 
3 columns, doesn't matter the width of the content,
we will always display 3 columns
*/
div {
column-count: 3;
}
|LiveURL=http://code.webplatform.org/gist/5305530
}}{{Single Example
|Language=CSS
|Description=Using auto for column-count will allow as many columns as are necessary or able to be generated.
|Code=/* auto column-count allows n-columns of column-width */
div {
column-count: auto;
column-width: 100px;
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The actual column count may vary from the value specified due to available space.
To ensure the specified value is used, all length property values of the multi-column element must be specified.
|Import_Notes====Syntax===
<code>'''column-count: '''''count'' '''{{!}}''' auto</code>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Multi-column Layout Module
|URL=http://www.w3.org/TR/css3-multicol/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row}}
}}
{{See_Also_Section
|Topic_clusters=Box Model, Multi-Column, Responsive Web Design
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>address</code>
*<code>blockQuote</code>
*<code>div</code>
*<code>dl</code>
*<code>fieldSet</code>
*<code>form</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>ol</code>
*<code>p</code>
*<code>pre</code>
*<code>[[html/elements/table|table]]</code>
*<code>ul</code>
*<code>dd</code>
*<code>dt</code>
*<code>li</code>
*<code>tBody</code>
*<code>td</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>button</code>
*<code>del</code>
*<code>ins</code>
*<code>map</code>
*<code>object</code>
*<code>script</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}