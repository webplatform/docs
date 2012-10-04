{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=multi-column elements
|Media=visual
|Inherited=No
|Initial value=none
|Values={{CSS_Property_Value|Data Type=none |Description=Default. No border is drawn, regardless of any specified [[css/properties/border-width|'''borderWidth''']].}}
{{CSS_Property_Value|Data Type=dotted |Description=Border is a dotted line.}}
{{CSS_Property_Value|Data Type=dashed |Description=Border is a dashed line.}}
{{CSS_Property_Value|Data Type=solid |Description=Border is a solid line.}}
{{CSS_Property_Value|Data Type=double |Description=Border is a double line drawn on top of the background of the object. The sum of the two single lines and the space between equals the [[css/properties/border-width|'''borderWidth''']] value. The border width must be at least 3 pixels wide to draw a double border.}}
{{CSS_Property_Value|Data Type=groove |Description=3-D groove is drawn in colors based on the value. The [[css/properties/border-width|'''borderWidth''']] property of the object must be specified for the style to render correctly.}}
{{CSS_Property_Value|Data Type=ridge |Description=3-D ridge is drawn in colors based on the value.}}
{{CSS_Property_Value|Data Type=inset |Description=3-D inset is drawn in colors based on the value.}}
{{CSS_Property_Value|Data Type=window-inset |Description=Internet Explorer 6 and later. 

Border is the same as inset, but is surrounded by an additional single line, drawn in colors based on the value.}}
{{CSS_Property_Value|Data Type=outset |Description=3-D outset is drawn in colors based on the value.}}
{{CSS_Property_Value|Data Type=hidden |Description=Internet Explorer 8.

Same as <code>none</code>, except in terms of conflict resolution of collapsed borders. Any element with a <code>hidden</code> border suppresses all shared borders at that location. Borders with a style of <code>none</code> have the lowest priority.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''column-rule-style: '''none '''{{!}}''' dotted '''{{!}}''' dashed '''{{!}}''' solid '''{{!}}''' double '''{{!}}''' groove '''{{!}}''' ridge '''{{!}}''' inset '''{{!}}''' window-inset '''{{!}}''' outset '''{{!}}''' hidden</code>
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
|Topic_clusters=Multi-Column
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}