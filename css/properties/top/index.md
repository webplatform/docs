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
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. Default position according to the regular HTML layout of the document.}}
{{CSS_Property_Value|Data Type=length |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a percent sign (%). This value is a percentage of the height of the parent object.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''top''' attribute and the '''top''' property to change the position of the object.

This example uses an inline style to set the position of a '''div''' object.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/top_h.htm
|Code=
&lt;DIV STYLE{{=}}"position:absolute;top:100px"&gt;
. . . &lt;/DIV&gt;
}}
{{Single_Example
|Description=This example uses inline script to change the position of the image set by an inline style. The change occurs during [[dom/events/mouseover|'''onmouseover''']] and [[dom/events/mouseout|'''onmouseout''']] events.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/top_s.htm
|Code=
&lt;IMG SRC{{=}}"cone.jpg" STYLE{{=}}"position:absolute; 
    top:80px;" onmouseover{{=}}"this.style.top{{=}}'100px''"    
    onmouseout{{=}}"this.style.top{{=}}'80px'" &gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''top''' attribute should be used only when the [[css/properties/position|'''position''']] attribute is set; otherwise, the value of the '''top''' attribute is ignored.
Because the value of the '''top''' property is a string, you cannot use the property in script to calculate the position of the object in the document; instead, use the [[css/cssom/properties/pixelTop|'''pixelTop''']] or the [[css/cssom/properties/posTop|'''posTop''']] property.
For more information about how to access the dimension and location of objects on the document through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes=
===Syntax===
<code>'''top: '''''
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
*<code>Reference</code>
*<code>[[css/cssom/properties/pixelTop|pixelTop]]</code>
*<code>[[css/cssom/properties/posTop|posTop]]</code>
|Topic_clusters=Box Model
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}