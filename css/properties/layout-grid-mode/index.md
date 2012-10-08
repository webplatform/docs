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
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=both
|Description=Default. Both the '''char''' and '''line''' grid modes are enabled. This setting is necessary to fully enable the layout grid on an element.
}}{{CSS Property Value
|Data Type=none
|Description=No grid is used.
}}{{CSS Property Value
|Data Type=line
|Description=Only a line grid is used. This is recommended for use with inline elements, such as a '''span''', to disable the horizontal grid on runs of text that act as a single entity in the grid layout.
}}{{CSS Property Value
|Data Type=char
|Description=Only a character grid is used. This is recommended for use with block-level elements, such as a '''blockquote''', where the line grid is intended to be disabled.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''-ms-layout-grid-mode''' attribute to specify character layout for a block of text.
|Code=&lt;STYLE&gt;
DIV.layout { layout-grid-mode: line }
&lt;/STYLE&gt;
&lt;DIV CLASS {{=}} "layout"&gt;
This is a block element containing a sentence of sample text.
&lt;/DIV&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-layout-grid-mode''' attribute is an extension to CSS, and can be used as a synonym for '''layout-grid-mode''' in IE8 Standards mode.
Web documents in Asian languages, such as Chinese or Japanese, usually create a page layout for characters using a one- or two-dimensional grid. You can use the [[css/properties/layout-grid|'''-ms-layout-grid''']] attribute to incorporate this layout into Web documents.
|Import_Notes====Syntax===
<code>'''-ms-layout-grid-mode: '''both '''{{!}}''' none '''{{!}}''' line '''{{!}}''' char</code>
===Standards information===
There are no standards that apply here.
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
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
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