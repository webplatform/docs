{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Fires the '''onerror''' event and passes the associated error to the '''error''' property.
Error codes map directly to World Wide Web Consortium (W3C) file errors, as described in the following table.
{{{!}} class="wikitable"
{{!}}-
!Type
!Description
{{!}}-
{{!}}NotFoundError
{{!}}The resource ([[apis/file/File|'''File''']], [[apis/file/Blob|'''Blob''']], or [[apis/file/MSStream|'''msStream''']]) could not be found at the time the read was processed.
{{!}}-
{{!}}SecurityError
{{!}}One of the following occurred:
*The file being accessed is unsafe.
*The file has changed since the user selected it.
*Other security issues not covered by other error types.

{{!}}-
{{!}}NotReadableError
{{!}}The resource could not be read. This may occur due to permission problems on the file.
{{!}}-
{{!}}EncodingError
{{!}}The resource could not be encoded due to data URL length limitations.
{{!}}}
 
This property is <code>null</code> unless there is an error.
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
*<code>[[apis/file/FileReader|FileReader]]</code>
*<code>[[apis/file/MSStreamReader|msStreamReader]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}