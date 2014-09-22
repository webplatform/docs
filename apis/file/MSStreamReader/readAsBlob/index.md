{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Non-standard; deletion candidate
|Checked_Out=No
|High-level issues=Deletion Candidate, Needs Review
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Performs an asynchronous read of an [[apis/file/MSStream|MSStream]] object in order to create a [[apis/file/Blob|Blob]] object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=
|Name=stream
|Data type=Blob
|Description=The [[apis/file/MSStream|MSStream]] object to read.
|Optional=No
}}{{Method Parameter
|Index=
|Name=maxSize
|Data type=Number
|Description=String that specifies the  maximum size of the  object to read.
|Optional=Yes
}}
|Method_applies_to=apis/file/MSStreamReader
|Example_object_name=MSStreamReader
|Return_value_name=
|Javascript_data_type=void
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=The '''readAsBlob''' method is used by [[apis/file/MSStreamReader|msStreamReader]] to create a [[apis/file/Blob|Blob]] object from an [[apis/file/MSStream|MSStream]]. When the read begins, the ''readyState'' property is set to the <code>LOADING</code> state on MSStreamReader and the ''onloadstart'' event is fired. Progress for the read is monitored by the ''onprogress'' event. When the read completes, the ''onloadend'' event fires and ''readyState'' is set to <code>DONE</code> and ''MSStreamReader.result'' returns the new Blob object.
A read operation can be interrupted if an error occurs or the ''abort'' method is run. If an error occurs, the ''onloadend'' event sets the ''readyState'' to <code>DONE</code>, and passes the error using the ''error'' property.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, FileAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}