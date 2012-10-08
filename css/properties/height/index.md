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
|Description=Default.  
}}{{CSS Property Value
|Data Type=height
|Description=Floating-point number followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer followed by a percent sign (%). The value is a percentage of the height of the parent object, which must be specified explicitly.  Negative values are not allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses an inline style sheet to set the height of an image to 4 centimeters.
|Code=&lt;img src{{=}}"sphere.jpg" style{{=}}"height: 4cm"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/height_h.htm
}}{{Single Example
|Description=This example uses inline scripting to change the height of an image when an [[dom/events/click|'''onclick''']] event occurs.
|Code=&lt;button onclick{{=}}"height1.style.height{{=}}'1cm'"&gt;Shrink sphere&lt;/button&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/height_s.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
If you specify the '''height''' property of an '''img''' object but not the [[css/properties/width|'''width''']] property, the width is proportional to the height according to the dimensions of the image source file.
To perform operations on the numeric value of this property, use [[css/cssom/properties/pixelHeight|'''pixelHeight''']] or [[css/cssom/properties/posHeight|'''posHeight''']].
As of Microsoft Internet Explorer 6, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, this property specifies the distance between the top and bottom edges of the content box—that is, within the [[css/properties/padding|'''padding''']].
When the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration does not specify standards-compliant mode, and with earlier versions of Windows Internet Explorer, this property includes the object's content box, plus the values of the following properties:
[[css/properties/border-top|'''border-top''']], 
[[css/properties/border-bottom|'''border-bottom''']], 
[[css/properties/padding-top|'''padding-top''']], and 
[[css/properties/padding-bottom|'''padding-bottom''']]. Subtracting the sum of the values of these properties from the value of the '''height''' property equals the height of the parent object's content box.
|Import_Notes====Syntax===
<code>'''height: '''height '''{{!}}''' percentage '''{{!}}''' auto</code>
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
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Conceptual</code>
*<code>Measuring Element Dimension and Location with CSSOM in Internet Explorer 9</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}