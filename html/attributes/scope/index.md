{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Notes_Section
|Notes=
===Remarks===
'''scope''' was introduced in Microsoft Internet Explorer 6
This property can be used for rendering to non-visual media such as speech or Braille.  It can also be used with style sheets.
The following table shows the possible values for this attribute as defined in [http://go.microsoft.com/fwlink/p/?linkid{{=}}203769 HTML 4.01] for '''td''' and '''th''' elements are:
{| class="wikitable"
|-
|row
|The current cell provides header information for its row.
|-
|col
|The current cell provides header information for its column.
|-
|rowgroup
|The header cell provides header information for its row.
|-
|colgroup
|The header cell provides header information for its column.
|}
 
This attribute may be used in place of the [[html/attributes/headers|'''headers''']] attribute.
There is no functionality implemented for this property unless defined by the author.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>td</code>
*<code>th</code>
*<code>[[html/attributes/headers|headers]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}