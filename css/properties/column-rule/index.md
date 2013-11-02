{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the width, style, and color of the rule between columns.}}
{{CSS Property
|Initial value=see individual properties
|Applies to=multi-column elements
|Inherited=No
|Media=visual
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=column-rule-width
|Description=Value of the [[css/properties/column-rule-width|'''column-rule-width''']] property.
}}{{CSS Property Value
|Data Type=column-rule-style
|Description=Value of the [[css/properties/column-rule-style|'''column-rule-style''']] property.
}}{{CSS Property Value
|Data Type=column-rule-color
|Description=Value of the [[css/properties/column-rule-color|'''column-rule-color''']] property.
}}{{CSS Property Value
|Data Type=transparent
|Description=Indicates rule is transparent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Makes 3 columns with 4px dashed green column-rule.
|Code=#columns {
  -moz-column-rule: 3; /* Firefox */
  -webkit-column-count: 3; /* Safari and Chrome */
  column-count: 3;
  -moz-column-rule: 4px dashed green; /* Firefox */
  -webkit-column-rule: 4px dashed green; /* Safari and Chrome */
  column-rule: 4px dashed green;
}
|LiveURL=http://code.webplatform.org/gist/6288958
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
<code>'''column-rule: '''''column-rule-width'' '''{{!}}{{!}}''' ''column-rule-style'' '''{{!}}{{!}}''' '''[''' ''column-rule-color'' '''{{!}}''' transparent ''']'''</code>
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