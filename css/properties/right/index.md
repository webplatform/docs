{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Position is determined by the regular HTML layout of the page.
}}{{CSS Property Value
|Data Type=length
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a percent sign (%). The value is a percentage of the width of the parent object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''right''' attribute to set a '''div''' object 50 pixels from the right of the client area.
|Code=&lt;DIV STYLE {{=}} "position:absolute; right:50px"&gt;
. . .
&lt;/DIV&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Only use the '''right''' attribute when the [[css/properties/position|'''position''']] attribute is set; otherwise, the value of the '''right''' attribute is ignored.
You cannot use the '''right''' property in script to calculate the position of the object in the document, because the value of the '''right''' property is a string. Instead, use the [[css/cssom/properties/pixelRight|'''pixelRight''']] property or the [[css/cssom/properties/posRight|'''posRight''']] property.
You cannot use the '''right''' property to calculate the position of the object in the document, because the value of the '''right''' property is a string.
For more information about how to access the dimension and location of objects on the page through the DHTML Object Model, see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes====Syntax===
<code>'''right: '''''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
'' '''{{!}}''' auto</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 9.3.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>LayoutRect</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}