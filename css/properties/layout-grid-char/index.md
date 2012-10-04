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
|Values={{CSS_Property_Value|Data Type=none |Description=Default. No character grid is set.}}
{{CSS_Property_Value|Data Type=auto |Description=Largest character in the font of the element is used to set the character grid.}}
{{CSS_Property_Value|Data Type=length |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer, followed by a percent sign (%). The value is a percentage derived from the dimensions of the parent object.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''-ms-layout-grid-char''' attribute to specify character layout for a block of text.
|LiveURL=
|Code=
&lt;STYLE&gt;
DIV.layout { layout-grid-char: auto }
&lt;/STYLE&gt;
&lt;DIV CLASS {{=}} "layout"&gt;
This is a block element containing a sentence of sample text.
&lt;/DIV&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-layout-grid-char''' attribute is an extension to CSS, and can be used as a synonym for '''layout-grid-char''' in IE8 Standards mode.
The visual effects of the '''-ms-layout-grid-char''' attribute are similar to the [[css/properties/line-height|'''line-height''']] property.
Web documents in Asian languages, such as Chinese or Japanese, usually create a page layout for characters using a one- or two-dimensional grid. You can use the [[css/properties/layout-grid|'''-ms-layout-grid''']] attribute to incorporate this layout into Web documents.
The '''-ms-layout-grid-char''' attribute applies only to block-level elements.
'''Note'''  For this property to have an effect, the [[css/properties/layout-grid-mode|'''-ms-layout-grid-mode''']] attribute must be set to '''line''' or '''both'''.
|Import_Notes=
===Syntax===
<code>'''-ms-layout-grid-char: '''none '''{{!}}''' auto '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
''</code>
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}