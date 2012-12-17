{{Page_Title}}
{{Flags}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Creates random access data (Blob) from an MSStream object.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes='''MSStreamReader''' is a constructor function producing an object that provides methods to asynchronously read an [[apis/file/MSStream|MSStream]], and an event model to obtain the results of these reads.
MSStreamReader lets you read and interact with MSStream objects.
MSStreamReader performs the conversion of  multimedia that is in a C++ file format into a format that can be accessed by JavaScript. The original file is accessed as an MSStream that overlays a Blob object.
MSStreamReader uses the ''readAsBlob'' method to perform an asynchronous read of data from the MSStream when converting it to a Blob. A series of events is used to track the progress of the read and any errors that occur.
The MSStreamReader can be in one of three states. The ''readyState'' returns the current state. The state is one of the following values:
*EMPTY. The MSStreamReader object has been created and there are no pending reads. This is the default state of a new MSStreamReader object until the ''readAsBlob'' method is called.
*LOADING. 
An MSStream is being read. The ''readAsBlob'' method is running and no error has occurred during the read.
*DONE. The entire MSStream has been read into memory, a file error occurred during the read, or the read was aborted using the ''abort'' method. The MSStreamReader is no longer reading an MSStream. If ''readyState'' is set to <code>DONE</code>, it means that the ''readAsBlob'' method has been called at least once.

When the MSStreamReader read operation is done on the MSStream, the ''result'' property returns the Blob object that contains the data buffered from the MSStream. The ''result'' is returned after the ''onloadend'' event has fired.
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