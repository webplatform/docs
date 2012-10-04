{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
An error that occurs during a call to the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method fires the '''onerror''' event and passes the associated error to the '''error''' property.
Error codes map directly to World Wide Web Consortium (W3C) file errors, as described in the following table.
{| class="wikitable"
|-
!Type
!Description
|-
|NotFoundError
|The resource ([[apis/file/File|'''File''']], [[apis/file/Blob|'''Blob''']], or [[apis/file/MSStream|'''msStream''']]) could not be found at the time the read was processed.
|-
|SecurityError
|One of the following occurred:
*The file being accessed is unsafe.
*The file has changed since the user selected it.
*Other security issues not covered by other error types.

|-
|NotReadableError
|The resource could not be read. This may occur due to permission problems on the file.
|-
|EncodingError
|The resource could not be encoded due to data URL length limitations.
|}
 
This property is <code>null</code> unless there is an error.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/file/FileReader|FileReader]]</code>
*<code>[[apis/file/MSStreamReader|msStreamReader]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}