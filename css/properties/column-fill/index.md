{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies how to fill columns, balanced or not.}}
{{CSS Property
|Initial value=balance
|Applies to=multi-column elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. 
Columns are filled sequentially such that the columns may differ in length,

depending on other column property values.
}}{{CSS Property Value
|Data Type=balance
|Description=Columns are filled sequentially such that the column heights are as balanced as possible,

depending on other column property values.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Makes as many 15em columns but  restrict the heights of the columns to 400px

|Code=/*
Makes as many 15em columns but  restrict the heights of the columns to 400px
*/
#column4 {
  column-width: 15em;
  column-gap: 2em;          
  column-rule: 4px solid green;
  padding: 5px;
  column-fill: balance;
  height: 400px;
}
|LiveURL=http://code.webplatform.org/gist/5305740
}}
}}
{{Notes_Section
|Notes====Remarks===
Column balancing is also dependent on the values of [[css/properties/orphans|'''orphans''']] and [[css/properties/widows|'''widows''']], if set.
|Import_Notes====Syntax===
<code>'''column-fill: '''auto '''{{!}}''' balance</code>
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Multi-Column
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