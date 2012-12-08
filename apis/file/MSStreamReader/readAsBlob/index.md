{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Performs an asynchronous read of an [[apis/file/MSStream|'''MSStream''']] object in order to create a [[apis/file/Blob|'''Blob''']] object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=stream
|Data type=Blob
|Description=The [[apis/file/MSStream|'''MSStream''']] object to read.
|Optional=No
}}{{Method Parameter
|Name=maxSize
|Data type=Number
|Description=String that specifies the  maximum size of the  object to read.
|Optional=Yes
}}
|Method_applies_to=apis/file/MSStreamReader
|Example_object_name=streamReader
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The '''readAsBlob''' method is used by [[apis/file/MSStreamReader|'''msStreamReader''']] to create a [[apis/file/Blob|'''Blob''']] object from an [[apis/file/MSStream|'''MSStream''']]. When the read begins, the [[apis/file/properties/readyState|'''readyState''']] property is set to the <code>LOADING</code> state on '''MSStreamReader''' and the [[apis/file/events/onloadstart|'''onloadstart''']] event is fired. Progress for the read is monitored by the [[apis/file/events/onprogress|'''onprogress''']] event. When the read completes, the [[apis/file/events/onloadend|'''onloadend''']] event fires and '''readyState''' is set to <code>DONE</code> and '''MSStreamReader'''.[[apis/file/properties/result|'''result''']] returns the new '''Blob''' object.
A read operation can be interrupted if an error occurs or the [[apis/file/methods/abort|'''abort''']] method is run. If an error occurs, the [[apis/file/events/onloadend|'''onloadend''']]event, sets the [[apis/file/properties/readyState|'''readyState''']] to <code>DONE</code>, and passes the error using the [[apis/file/properties/error|'''error''']] property.
For a code example, see [[apis/file/MSStreamReader|'''MSStreamReader''']].
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}