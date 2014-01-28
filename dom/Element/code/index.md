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
The <code>code</code> property returns one of the following file error codes.
{{{!}} class="wikitable"
{{!}}-
!Constant
!Code
!Description
{{!}}-
{{!}}NotFoundError
{{!}}8
{{!}}The [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] could not be found at the time the read was processed.
{{!}}-
{{!}}SecurityError
{{!}}18
{{!}}A file error not covered by the other file error codes occurred, such as:
*Too many read calls are being made on [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] resources.
*The file has changed on disk since the user selected it.
*Certain files are unsafe for access within a web application.

{{!}}-
{{!}}AbortError
{{!}}20
{{!}}The read operation was aborted, typically with a call to [[apis/file/methods/abort|'''abort''']].
{{!}}-
{{!}}NotReadableError
{{!}}0
{{!}}The [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] cannot be read, typically due to permission problems that occur after a reference to a '''File''' or '''Blob''' has been acquired (that is, concurrent lock with another application).
{{!}}-
{{!}}EncodingError
{{!}}0
{{!}}The length of the data URL for a [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] is too long.
{{!}}}
 
See [[apis/file/FileError|'''FileError''']] for a code example using these error codes.
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
*<code>[[apis/file/FileError|FileError]]</code>
*<code>[[apis/file/MSStreamError|MSStreamError]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}