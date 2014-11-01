{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add summery, specifications, compatibility.
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=both loose none none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=
|Animatable=No
|CSS object model property=
|CSS percentages=
|Values={{CSS Property Value
|Data Type=mode
|Description=Any of the range of mode values available to the [[css/properties/layout-grid-mode|'''-ms-layout-grid-mode''']] property.
}}{{CSS Property Value
|Data Type=type
|Description=Any of the range of type values available to the [[css/properties/layout-grid-type|'''-ms-layout-grid-type''']] property.
}}{{CSS Property Value
|Data Type=line
|Description=Any of the range of line values available to the [[css/properties/layout-grid-line|'''-ms-layout-grid-line''']] property.
}}{{CSS Property Value
|Data Type=char
|Description=Any of the range of character values available to the [[css/properties/layout-grid-char|'''-ms-layout-grid-char''']] property.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''-ms-layout-grid''' attribute to specify character layout for a block of text.
|Code=&lt;STYLE&gt;
DIV.layout { layout-grid: both fixed 12px 12px }
&lt;/STYLE&gt;
&lt;DIV CLASS {{=}} "layout"&gt;
This is a block element containing a sentence of sample text.
&lt;/DIV&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-layout-grid''' attribute is an extension to CSS, and can be used as a synonym for '''layout-grid''' in IE8 Standards mode.
Though you don't have to specify all four values for the '''-ms-layout-grid''' attribute, they must be listed in the order given in Possible Values.
Web documents in Asian languages, such as Chinese or Japanese, usually create a page layout for characters using a one-dimensional or two-dimensional grid. You can use the '''-ms-layout-grid''' attribute to incorporate this layout into Web documents.
|Import_Notes====Syntax===
<code>'''-ms-layout-grid: '''mode type line char</code>
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/HTMLOptionElement/defaultSelected|defaultSelected]]</code>
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}