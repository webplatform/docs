{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=show |Description=Renders empty cells with inherited borders and styles}}
{{CSS_Property_Value|Data Type=hide |Description=Does not render the cell}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
If all cells in a particular row have the '''empty-cells''' value set to '''hide''', the entire row will behave as if it had the [[css/properties/display|'''display''']] value of <code>none</code>.
The '''empty-cells''' value can be set for an entire table.  If the value is set in the [[html/elements/table|'''table''']] properties to <code>show</code>,all cells will be rendered with borders, regardless of their content.
|Import_Notes=
===Syntax===
<code>'''empty-cells: '''show '''{{!}}''' hide</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 17.6.1.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Tables
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}