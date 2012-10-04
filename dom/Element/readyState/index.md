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
You must return the state of [[apis/file/MSStreamReader|'''msStreamReader''']] when getting the object. '''readyState''' is set only when the '''msStreamReader''' is created and by the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method.
When the [[apis/file/MSStreamReader|'''msStreamReader''']] object is created, the state is set to <code>EMPTY</code>. When there is a call to the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method, the state is set to <code>LOADING</code>. If '''readyState''' is set to <code>DONE</code>, it means that the '''readAsBlob''' method has been called at least once.
The [[apis/file/FileReader|'''FileReader''']] object can be in one of three states.
{| class="wikitable"
|-
!Constant
!Value
!Description
|-
|EMPTY
|0
|The [[apis/file/FileReader|'''FileReader''']] object has been constructed, and there are no pending reads. None of the read methods have been called. This is the default state of a newly created '''FileReader''' object, until one of the read methods has been called on it.
|-
|LOADING
|1
|A [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] is being read. One of the read methods is being processed, and no error has occurred during the read.
|-
|DONE
|2
|The entire [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] has been read into memory, a file error occurred during read, or the read was aborted using [[apis/file/methods/abort|'''abort''']]. The [[apis/file/FileReader|'''FileReader''']] is no longer reading a '''File''' or '''Blob'''. If <code>readyState</code> is set to <code>DONE</code> it means at least one of the read methods have been called on this '''FileReader''' object.
|}
 
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