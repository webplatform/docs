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
The format of the <code>result</code> data depends on which of the read methods was used to initiate the read operation. This property can also return partial [[apis/file/Blob|'''Blob''']] data. Partial '''Blob''' data is the part of the [[apis/file/File|'''File''']] or '''Blob''' that has been read into memory currently; when processing the read method [[apis/file/methods/readAsText (File and Blob)|'''readAsText''']], partial '''Blob''' data is a Document Object Model (DOM) string that is incremented as more bytes are loaded; and when processing [[apis/file/methods/readAsArrayBuffer|'''readAsArrayBuffer''']], partial '''Blob''' data is an array buffer object consisting of the bytes loaded so far.
When a call is made to the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method, the data that is read from the [[apis/file/MSStream|'''msStream''']] is returned as a [[apis/file/Blob|'''Blob''']] object. If the read by '''readAsBlob''' is interrupted due to an error or an [[apis/file/methods/abort|'''abort''']], or if the '''msStream''' is empty, a <code>null</code> is returned by '''result'''. If the read is successful, the [[apis/file/events/onloadend|'''onloadend''']] event fires and the  '''Blob''' object is returned by '''result'''.
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