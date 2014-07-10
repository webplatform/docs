{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''ENCTYPE''' attribute of the form specifies how the HTTP request should be encoded. All GET requests are submitted as '''application/x-www-form-urlencoded'''. The value of '''multipart/form-data''' is required (with a POST request) to submit a file to the server. The value of '''text/plain''' forces the request to be POST.
Windows Internet Explorer 8 and later. In IE8 Standards mode, the '''enctype''' Document Object Model (DOM) attribute is now supported and reflects the '''ENCTYPE''' content attribute. For more information, see Attribute Differences in Internet Explorer 8.
The '''enctype''' property was introduced in Internet Explorer 8. If backward compatibility is required, use the [[html/attributes/encoding|'''encoding''']] property.
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>form</code>
*<code>[[html/attributes/encoding|encoding]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}