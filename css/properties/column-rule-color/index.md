{{Page_Title}}
{{Flags
|Content=Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies the color of the rule between columns.}}
{{CSS Property
|Initial value=currentColor
|Applies to=multi-column elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=columnRuleColor
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=color
|Description=One of the color names or RGB values in the [[css/color/color table|Color Table]].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Uses the column-rule attribute to set rule width, style and color
|Code=#column3 {
  column-width: 15em;
  column-gap: 2em;
/*
The column-rule attribute is a shorthand for

column-rule-width = 4px
column-rule-style = solid
column-rule-color = green
*/
  column-rule: 4px solid green;
  padding: 5px;
}
|LiveURL=http://code.webplatform.org/gist/5305898
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
<code>'''column-rule-color: '''''
&lt;color&gt;
''</code>
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