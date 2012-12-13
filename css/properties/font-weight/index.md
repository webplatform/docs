{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets or sets the weight of the font of the object (for example, bolder or lighter than normal).}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Font is normal.
}}{{CSS Property Value
|Data Type=bold
|Description=Font is bold.
}}{{CSS Property Value
|Data Type=bolder
|Description=Font is at least as bold as the default '''bold''' weight.
}}{{CSS Property Value
|Data Type=lighter
|Description=Font is lighter than normal.
}}{{CSS Property Value
|Data Type=100
|Description=Font is at least as light as the 200 weight.
}}{{CSS Property Value
|Data Type=200
|Description=Font is at least as bold as the 100 weight and at least as light as the 300 weight.
}}{{CSS Property Value
|Data Type=300
|Description=Font is at least as bold as the 200 weight and at least as light as the 400 weight.
}}{{CSS Property Value
|Data Type=400
|Description=Font is normal.
}}{{CSS Property Value
|Data Type=500
|Description=Font is at least as bold as the 400 weight and at least as light as the 600 weight.
}}{{CSS Property Value
|Data Type=600
|Description=Font is at least as bold as the 500 weight and at least as light as the 700 weight.
}}{{CSS Property Value
|Data Type=700
|Description=Font is bold.
}}{{CSS Property Value
|Data Type=800
|Description=Font is at least as bold as the 700 weight and at least as light as the 900 weight.
}}{{CSS Property Value
|Data Type=900
|Description=Font is at least as bold as the 800 weight.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''font-weight''' attribute and the '''font-weight''' property to change the font weight.

This example uses '''li''' as a selector in an embedded (global) style sheet to set the font weight to '''bolder'''.
|Code=&lt;STYLE&gt;
LI { font-weight:bolder }
&lt;/STYLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font-weight.htm
}}{{Single Example
|Description=This example uses inline scripting to set the font weight to '''bolder''' when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;P STYLE{{=}}"font-size:14" onmouseover{{=}}"this.style.fontWeight{{=}}'bolder'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontWeight.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Keywords for '''font-weight''' values are mapped to specific font variations depending on the fonts that are installed on the user's computer. In many cases, the user cannot see the difference between different '''font-weight''' settings because the system chooses the closest match.
Setting the '''font-weight''' to '''400''' is equivalent to '''normal''', and to '''700''' is equivalent to '''bold'''. An '''font-weight''' of '''bolder''' or '''lighter''' is interpreted relative to the parent object's weight. A value of '''bolder''' for text whose parent is normal sets the text to bold.
To convert these strings to numeric equivalents, use the read-only [[css/cssom/properties/fontWeight|'''fontWeight''']] property.
Microsoft Internet Explorer 4.0 supports only '''normal''' and '''bold'''.
Microsoft Internet Explorer 3.0 supports the '''font-weight''' attribute through the [[css/properties/font|'''font''']] attribute.
|Import_Notes====Syntax===
<code>'''font-weight: '''normal '''{{!}}''' bold '''{{!}}''' bolder '''{{!}}''' lighter '''{{!}}''' 100 '''{{!}}''' 200 '''{{!}}''' 300 '''{{!}}''' 400 '''{{!}}''' 500 '''{{!}}''' 600 '''{{!}}''' 700 '''{{!}}''' 800 '''{{!}}''' 900</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.2.5
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
|Topic_clusters=Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/font|font]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}