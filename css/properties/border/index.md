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
|Values={{CSS_Property_Value|Data Type=width |Description=Any of the range of width values available to the [[css/properties/border-width|'''border-width''']] property.}}
{{CSS_Property_Value|Data Type=style |Description=Any of the range of style values available to the [[css/properties/border-style|'''border-style''']] property.}}
{{CSS_Property_Value|Data Type=color |Description=Any of the range of color values available to the [[css/properties/border-color|'''border-color''']] property.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''border''' attribute and the '''border''' property to specify the composite border properties.

This example uses a call to an embedded (global) style sheet to modify the '''border''' attribute.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border_h.htm
|Code=
&lt;HEAD&gt;
&lt;STYLE&gt;
    .applyBorder { border:0.2cm groove orange }
    .removeBorder { border:none }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE BORDER&gt;
&lt;TR&gt; 
    &lt;TD onmouseover{{=}}"this.className{{=}}'applyBorder'"
        onmouseout{{=}}"this.className{{=}}'removeBorder'"&gt;
    &lt;IMG src{{=}}"sphere.jpg"&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to modify the '''border''' property.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border_s.htm
|Code=
&lt;TD onmouseover{{=}}"this.style.border{{=}}'0.2cm groove pink'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''border''' property is a composite property that sets the '''width''', '''style''', and '''color''' values for all four sides of an object.
You must specify a '''style''' when specifying a '''width''' or '''color'''; otherwise, the border does not render.
All individual border properties not set by the composite border property are set to their default values. For example, the default value for '''width''' is '''medium'''.
The setting '''border'''{{=}}'''thin''' is identical to '''border'''{{=}}'''thin''' '''none'''; the default value for the border color is the same as the text color if one is not initially set. So, not only does the property set '''width''' to '''thin''', it also clears any '''style''' or '''color''' values previously set.
Setting a border to zero or omitting the attribute causes no border to be displayed. Supplying the border attribute without a value defaults to a single border.
If a '''color''' is not specified, the text color is used.
For more information about supported colors, see the Color Table.
The '''border''' property also applies to '''input'''; however, it has no actual function in Windows Internet Explorer, and '''border''' has been deprecated in favor of the appropriate CSS markup (see [http://go.microsoft.com/fwlink/p/?linkid{{=}}203728 Cascading Style Sheets (CSS)]).
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes=
===Syntax===
<code>'''border: ''''''[''' width '''{{!}}{{!}}''' style '''{{!}}{{!}}''' ''
&lt;color&gt;
'' ''']'''</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
|Topic_clusters=Border
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}