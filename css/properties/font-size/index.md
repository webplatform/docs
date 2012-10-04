{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=medium
|Values={{CSS_Property_Value|Data Type=absolute-size |Description=Set of keywords that indicate predefined font sizes. Named font sizes scale according to the user's font setting preferences. Possible values include the following: xx-small, x-small, small, medium, large, x-large, xx-large.}}
{{CSS_Property_Value|Data Type=relative-size |Description=Set of keywords that are interpreted as relative to the font size of the parent object. Possible values include the following: smaller, larger.}}
{{CSS_Property_Value|Data Type=length |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>).
For more information about the supported length units, see the CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a percent (%). The value is a percentage of the parent object's font size. In Internet Explorer 3.0, the value is calculated as a percentage of the default font size.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''font-size''' attribute and the '''font-size''' property to change font characteristics.

This example sets the font size on several paragraphs using different size values.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font-size.htm
|Code=
&lt;STYLE&gt;
   BODY{font-size: 10pt }
   .P1 {font-size: 14pt }
   .P2 {font-size: 75% }
   .P3 {font-size: xx-large }
   .P4 {font-size: larger }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the font size to <code>14pt</code> when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontSize.htm
|Code=
&lt;DIV STYLE{{=}}"font-size:12pt" onmouseover{{=}}"this.style.fontSize{{=}}'14pt'"&gt;
:
&lt;/DIV&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Negative values are not allowed. Font sizes using the proportional "em" measure are based on the font size of the parent object.
As of Microsoft Internet Explorer 6, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, the default value for this property is <code>medium</code>, not <code>small</code>.
Possible length values specified in a relative measurement, using the height of the element's font (em) or the height of the letter "x" (ex), are supported in Microsoft Internet Explorer 4.0 and later.
|Import_Notes=
===Syntax===
<code>'''font-size: '''''
&lt;absolute-size&gt;
'' '''{{!}}''' ''
&lt;relative-size&gt;
'' '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
''</code>
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
*<code>[[css/properties/font|font]]</code>
*<code>Conceptual</code>
*<code>CSS Values and Units Reference</code>
|Topic_clusters=Fonts
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}