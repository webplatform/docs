{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Aborts a read operation by reader objects, like [[apis/file/FileReder|FileReader]].}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/file/FileReader
|Example_object_name=reader
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The '''abort''' method is used to interrupt an asynchronous  read operation that is in progress on an [[apis/file/events/onloadend|'''onloadend''']] event, sets the state of the [[apis/file/properties/readyState|'''readyState''']] property of the  '''MSStreamReader''' or [[apis/file/FileReader|'''FileReader''']] to <code>DONE</code>, and sets [[apis/file/properties/result|'''result''']] property to <code>null</code>.
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
*<code>[[apis/file/MSStreamReader|MSStreamReader]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}