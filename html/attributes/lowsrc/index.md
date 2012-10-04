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
If the [[html/attributes/src|'''src''']] property is set in code, the new URL starts loading into the image area and aborts the transfer of any image data that is already loading into the same area. If you want to alter the '''lowsrc''' property, you must do so before setting the '''src''' property. If the URL in the '''src''' property references an image that is not the same size as the image cell it is loaded into, the source image is scaled to fit.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>img</code>
*<code>input</code>
*<code>input type{{=}}image</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}