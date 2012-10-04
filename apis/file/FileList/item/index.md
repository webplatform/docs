{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=index|Data type=unsigned long|Description=The [[apis/file/FileList|'''FileList''']] index (starting from 0) of the [[apis/file/File|''' File''']] object to return.|Optional=}}
{{Method Parameter|Name=retVal|Data type=File|Description=|Optional=}}
|Method_applies_to=apis/file/FileList
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The first [[apis/file/File|'''File''']] object in a [[apis/file/FileList|'''list of files''']] called <code>selectedFiles</code> can be accessed by either of the following methods:
*<code>selectedFiles.item(0)</code>
*<code>selectedFiles[0]</code>

|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/file/FileList|FileList]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}