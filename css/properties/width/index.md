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
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. Default width of the object.}}
{{CSS_Property_Value|Data Type=width |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a %. The value is a percentage of the width of the parent object, whether or not it is specified explicitly.  Negative values are not allowed.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses an inline style sheet to set the width of an image.The following examples use the '''width''' attribute and the '''width''' property to change the width of the object.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/width_h.htm
|Code=
&lt;DIV STYLE{{=}}"position:absolute;top:10px;left:10px;width:1in"&gt;
. . . &lt;/DIV&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the width of an image when an [[dom/events/click|'''onclick''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/width_s.htm
|Code=
&lt;IMG SRC{{=}}"sphere.jpg" onclick{{=}}"this.style.width{{=}}'1cm'"
    ondblclick{{=}}"this.style.width{{=}}''"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
As of Microsoft Internet Explorer 6, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, this property specifies the distance between the left and right edges of the content box—that is, within the [[css/properties/padding|'''padding''']].
When the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration does not specify standards-compliant mode, and with earlier versions of Windows Internet Explorer, this property includes the object's content box, plus the values of the following properties:  [[css/properties/border-left|'''border-left''']], [[css/properties/border-right|'''border-right''']], [[css/properties/padding-left|'''padding-left''']], and [[css/properties/padding-right|'''padding-right''']].  Subtracting the sum of the values of these properties from the value of the '''width''' property equals the width of the parent object's content box.
To perform operations on the numeric value of this property, use [[css/cssom/properties/pixelWidth|'''pixelWidth''']] or [[css/cssom/properties/posWidth|'''posWidth''']].
For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes=
===Syntax===
<code>'''width: '''auto '''{{!}}''' width '''{{!}}''' percentage</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Conceptual</code>
*<code>Measuring Element Dimension and Location with CSSOM in Internet Explorer 9</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
|Topic_clusters=Background, Box Model
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}