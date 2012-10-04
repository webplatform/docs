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
The '''ENCTYPE''' attribute of the form specifies how the HTTP request should be encoded. All GET requests are submitted as '''application/x-www-form-urlencoded'''. The value of '''multipart/form-data''' is required (with a POST request) to submit a file to the server. The value of '''text/plain''' forces the request to be POST.
Windows Internet Explorer 8 and later. In IE8 Standards mode, the '''enctype''' Document Object Model (DOM) attribute is now supported and reflects the '''ENCTYPE''' content attribute. For more information, see Attribute Differences in Internet Explorer 8.
The '''enctype''' property was introduced in Internet Explorer 8. If backward compatibility is required, use the [[html/attributes/encoding|'''encoding''']] property.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>form</code>
*<code>[[html/attributes/encoding|encoding]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}