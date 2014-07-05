{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs summary, examples, specs and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
The format of the <code>result</code> data depends on which of the read methods was used to initiate the read operation. This property can also return partial [[apis/file/Blob|'''Blob''']] data. Partial '''Blob''' data is the part of the [[apis/file/File|'''File''']] or '''Blob''' that has been read into memory currently; when processing the read method [[apis/file/FileReader/readAsText|'''readAsText''']], partial '''Blob''' data is a Document Object Model (DOM) string that is incremented as more bytes are loaded; and when processing [[apis/file/FileReader/readAsArrayBuffer|'''readAsArrayBuffer''']], partial '''Blob''' data is an array buffer object consisting of the bytes loaded so far.
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
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}