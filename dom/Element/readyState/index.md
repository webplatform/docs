{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs summary, examples, spec, and compat
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
The [[apis/file/FileReader|'''FileReader''']] object can be in one of three states.
{{{!}} class="wikitable"
{{!}}-
!Constant
!Value
!Description
{{!}}-
{{!}}EMPTY
{{!}}0
{{!}}The [[apis/file/FileReader|'''FileReader''']] object has been constructed, and there are no pending reads. None of the read methods have been called. This is the default state of a newly created '''FileReader''' object, until one of the read methods has been called on it.
{{!}}-
{{!}}LOADING
{{!}}1
{{!}}A [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] is being read. One of the read methods is being processed, and no error has occurred during the read.
{{!}}-
{{!}}DONE
{{!}}2
{{!}}The entire [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] has been read into memory, a file error occurred during read, or the read was aborted using [[apis/file/FileReader/abort|'''abort''']]. The [[apis/file/FileReader|'''FileReader''']] is no longer reading a '''File''' or '''Blob'''. If <code>readyState</code> is set to <code>DONE</code> it means at least one of the read methods have been called on this '''FileReader''' object.
{{!}}}
 
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