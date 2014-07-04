{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets or sets the weight of the font of the object.}}
{{API_Object_Property
|Property_applies_to=css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
|Read_only=No
|Example_object_name=declaration
|Return_value_name=fontWeightValue
|Javascript_data_type=String
|Return_value_description=The current state of the value of the font-weight CSS property.
|Example_value_name=fontWeightValue
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example demonstrates how to set the [[css/properties/font-weight|'''fontWeight''']] property of a '''p''' element. The script reads the '''fontWeight''' property of the [[css/cssom/currentStyle|'''currentStyle''']] object and displays the value in a '''span''' element.
|Code=&lt;body onload{{=}}"setInterval('s1.innerText {{=}} p1.currentStyle.fontWeight',200)"&gt;
&lt;p id{{=}}"p1"&gt;Click the buttons below.&lt;/p&gt;
&lt;button onclick{{=}}"p1.style.fontWeight{{=}}'lighter';"&gt;Lighter&lt;/button&gt;
&lt;button onclick{{=}}"p1.style.fontWeight{{=}}'normal';"&gt;Normal&lt;/button&gt;
&lt;button onclick{{=}}"p1.style.fontWeight{{=}}'bold';"&gt;Bold&lt;/button&gt;
&lt;button onclick{{=}}"p1.style.fontWeight{{=}}'bolder';"&gt;Bolder&lt;/button&gt;
&lt;br&gt;Current Weight: &lt;span id{{=}}"s1"&gt;&lt;/span&gt;
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontWeight_1.htm
}}
}}
{{Notes_Section
|Notes=The '''fontWeight''' property of the [[css/cssom/currentStyle|'''currentStyle''']] object is read-only. To set the value, use the [[css/properties/font-weight|'''fontWeight''']] property of the [[css/cssom/style|'''style''']] object. Unlike the '''style''' object, the '''fontWeight''' property of the '''currentStyle''' object only returns numeric values.
Unlike [[css/properties/font-weight|'''fontWeight''']], '''fontWeight''' is read-only and returns only numeric values.
The values for '''fontWeight''' are mapped to specific font variations, depending on the fonts that are installed on the user's computer. In many cases, the user cannot see the difference between different '''fontWeight''' settings because the system chooses the closest match.
|Import_Notes====Syntax===
<code>'''fontWeight: '''100 '''{{!}}''' 200 '''{{!}}''' 300 '''{{!}}''' 400 '''{{!}}''' 500 '''{{!}}''' 600 '''{{!}}''' 700 '''{{!}}''' 800 '''{{!}}''' 900</code>
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
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>Reference</code>
*<code>[[css/properties/font-weight|fontWeight]]</code>
*<code>[[css/properties/font|font]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}