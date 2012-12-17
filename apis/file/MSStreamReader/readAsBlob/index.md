{{Page_Title}}
{{Flags}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Performs an asynchronous read of an [[apis/file/MSStream|MSStream]] object in order to create a [[apis/file/Blob|Blob]] object.}}
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
|Example_object_name=MSStreamReader
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The '''readAsBlob''' method is used by [[apis/file/MSStreamReader|msStreamReader]] to create a [[apis/file/Blob|Blob]] object from an [[apis/file/MSStream|MSStream]]. When the read begins, the ''readyState'' property is set to the <code>LOADING</code> state on MSStreamReader and the ''onloadstart'' event is fired. Progress for the read is monitored by the ''onprogress'' event. When the read completes, the ''onloadend'' event fires and ''readyState'' is set to <code>DONE</code> and ''MSStreamReader.result'' returns the new Blob object.
A read operation can be interrupted if an error occurs or the ''abort'' method is run. If an error occurs, the ''onloadend'' event sets the ''readyState'' to <code>DONE</code>, and passes the error using the ''error'' property.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|FileAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}