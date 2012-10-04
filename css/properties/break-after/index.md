{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=block-level elements
|Media=paged
|Inherited=No
|Initial value=auto
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. A page break or column break is determined  by the flow of content.}}
{{CSS_Property_Value|Data Type=always |Description=A page break is inserted (forced) after the content block.}}
{{CSS_Property_Value|Data Type=avoid |Description=A page break or column break is not allowed after the content block.}}
{{CSS_Property_Value|Data Type=left |Description=A page break is inserted (forced) after the content block such that the flow of content continues in the first column of the "left" page that immediately follows the current page (according to the paging format of the document).}}
{{CSS_Property_Value|Data Type=right |Description=A page break is inserted (forced) after the content block such that the flow of content continues in the first column of the "right" page that immediately follows the current page (according to the paging format of the document).}}
{{CSS_Property_Value|Data Type=page |Description=A page break is inserted (forced) after the content block such that the flow of content continues in the first column of the page that immediately follows the current page (according to the paging format of the document).}}
{{CSS_Property_Value|Data Type=column |Description=A column break is inserted (forced) after the content block.}}
{{CSS_Property_Value|Data Type=avoid-page |Description=A page break is not allowed after the content block.}}
{{CSS_Property_Value|Data Type=avoid-column |Description=A column break is not allowed after the content block.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''break-after: '''auto '''{{!}}''' always '''{{!}}''' avoid '''{{!}}''' left '''{{!}}''' right '''{{!}}''' page '''{{!}}''' column '''{{!}}''' avoid-page '''{{!}}''' avoid-column</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
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
*<code>Reference</code>
*<code>[[css/properties/break-before|breakBefore]]</code>
*<code>[[css/properties/break-inside|breakInside]]</code>
|Topic_clusters=Multi-Column
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}