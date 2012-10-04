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
|Values={{CSS_Property_Value|Data Type=transparent |Description=Default. Color of the next parent object through which the background is visible.}}
{{CSS_Property_Value|Data Type=color |Description=Any color value, including those specified in the Color Table.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''background-color''' attribute and the '''background-color''' property to specify the background color.

This example uses an inline style sheet to set the background color to <code>lime</code>.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-color.htm
|Code=
&lt;span style{{=}}"font-size: 14px; background-color: lime"&gt;The background color of the text has been set inline using the &lt;b&gt;background-color&lt;/b&gt; attribute.&lt;/span&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the background color to <code>lime</code>.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundColor.htm
|Code=
&lt;span style{{=}}"font-size: 14px" onmouseover{{=}}"this.style.backgroundColor{{=}}'lime'" onclick{{=}}"this.style.backgroundColor{{=}}'orange'" ondblclick{{=}}"this.style.backgroundColor{{=}}''"&gt;
    Run your mouse over this text to change the background color to lime. Click 
    to turn orange. Double-click to return to the default color. &lt;/span&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property can be set with the other background properties by using the [[css/cssom/properties/background|'''background''']] composite property.
Microsoft Internet Explorer 3.0 supports the '''background-color''' attribute, but only when it's set by using the [[css/cssom/properties/background|'''background''']] attribute.
In Windows CE, specifying a value for the '''background-color''' property of the '''OPTION''' element when applied through the [[css/cssom/style|'''style''']] object has no effect.
|Import_Notes=
===Syntax===
<code>'''background-color: '''''
&lt;color&gt;
'' '''{{!}}''' transparent</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Background
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}