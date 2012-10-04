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
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. Default position, according to the regular HTML layout of the page.}}
{{CSS_Property_Value|Data Type=length |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a percent sign (%). The value is a percentage of the width of the parent object.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''left''' attribute and the '''left''' property to change the position of the object.

This example uses an inline style sheet to set the position of an image 100 pixels to the right of the parent object's left edge.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/left_h.htm
|Code=
&lt;DIV STYLE{{=}}"position:absolute;left:100px"&gt;
&lt;IMG SRC{{=}}"cone.jpg"&gt;&lt;/DIV&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to change the position of two images when an [[dom/events/click|'''onclick''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/left_s.htm
|Code=
&lt;BUTTON onclick{{=}}"cone.style.left{{=}}'100px'; sphere.style.left{{=}}'200px'"&gt;
. . .&lt;/BUTTON&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You should use the '''left''' attribute only when the [[css/properties/position|'''position''']] attribute is set; otherwise, the value of the '''left''' attribute is ignored.
Because the value of the '''left''' property is a string, you cannot use the property in script to calculate the position of the object in the document; instead, you should use the [[css/cssom/properties/pixelLeft|'''pixelLeft''']] property or the [[css/cssom/properties/posLeft|'''posLeft''']] property.
Because the value of the '''left''' property is a string, you cannot use the property to calculate the position of the object in the document.
Because the value of the '''left''' property is a string, you cannot use the property in script to calculate the position of the object in the document; instead, you should use the [[css/cssom/properties/pixelLeft|'''pixelLeft''']] property or the [[css/cssom/properties/posLeft|'''posLeft''']] property.
For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes=
===Syntax===
<code>'''left: '''''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
'' '''{{!}}''' auto</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 9.3.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Box Model
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}