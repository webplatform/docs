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
|Values={{CSS_Property_Value|Data Type=length |Description=A floating-point number, followed by either an absolute units designator
(<code>cm</code>,
<code>mm</code>,
<code>in</code>,
<code>pt</code>,
or <code>pc</code>)
or a relative units designator
(<code>em</code>,
<code>ex</code>,
or <code>px</code>).
For more information about the supported length units,
see CSS Values and Units Reference.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
The length values specify the distance that separates adjoining cell borders.
If one length is specified, it represents both the horizontal and vertical spacing.
If two are specified, the first represents the horizontal spacing,
the second the vertical spacing. Negative lengths are ignored.
The distance between the table border and the borders of the cells
on the edge of the table is the
[[css/properties/padding|'''padding''']]
of the table for that side, plus the relevant
'''border-spacing''' distance.
For example, on the right side the distance is
[[css/properties/padding-right|'''padding-right''']]
plus the horizontal '''border-spacing'''.
This property requires Windows Internet Explorer to be in IE8 Standards mode rendering.
|Import_Notes=
===Syntax===
<code>'''border-spacing: '''''
&lt;length&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 17.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border-collapse|border-collapse]]</code>
|Topic_clusters=Tables
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}