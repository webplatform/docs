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
|Initial value=
|Values={{CSS_Property_Value|Data Type=loose |Description=Default. Grid used for Japanese and Korean characters. In this mode, a constant width increment is applied to characters as follows: Wide characters and narrow kana characters are incremented to obtain an exact grid fit, as specified by the [[css/properties/layout-grid-char|'''-ms-layout-grid-char''']] property.  Other narrow characters, except connected and cursive characters, are incremented by half of the increment amount applied to wide characters.  Other characters, including connected and  cursive characters, are not incremented, and behave as if no character grid is set.}}
{{CSS_Property_Value|Data Type=strict |Description=Grid used for Chinese, as well as Japanese (Genko) and Korean characters. Only the ideographs, kanas, and wide characters are snapped to the grid. Other characters are rendered as usual, as though the [[css/properties/layout-grid-mode|'''-ms-layout-grid-mode''']] attribute is set to '''none''' or '''line''' for text spans containing these characters. This mode also disables special text justification and character width adjustments normally applied to the element. Finally, if there is no line-break opportunity in a text span that exceeds the line boundary, the text is pushed to the next line and the last part of the previous line is left blank.}}
{{CSS_Property_Value|Data Type=fixed |Description=Grid used for monospaced layout. The layout rules are as follows:  All noncursive characters are treated as equal; every character is centered within a single grid space by default.  Runs of cursive characters are treated as strips the same as in a '''strict''' grid.  Justification or any other character-width changing behaviors are disabled.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''-ms-layout-grid-type''' attribute to specify character layout for a block of text.
|LiveURL=
|Code=
&lt;STYLE&gt;
DIV.layout { layout-grid-type: strict }
&lt;/STYLE&gt;
&lt;DIV CLASS {{=}} "layout"&gt;
This is a block element containing a sentence of sample text.
&lt;/DIV&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-layout-grid-type''' attribute is an extension to CSS, and can be used as a synonym for '''layout-grid-type''' in IE8 Standards mode.
Web documents in Asian languages, such as Chinese or Japanese, usually create a page layout for characters using a one- or two-dimensional grid. You can use the [[css/properties/layout-grid|'''-ms-layout-grid''']] attribute to incorporate this layout into Web documents.
The '''-ms-layout-grid-type''' attribute applies only to block-level elements.
|Import_Notes=
===Syntax===
<code>'''-ms-layout-grid-type: '''loose '''{{!}}''' strict '''{{!}}''' fixed</code>
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