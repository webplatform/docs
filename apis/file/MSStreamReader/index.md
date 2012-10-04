{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
'''MSStreamReader''' is a constructor function producing an object that provides methods to asynchronously read an [[apis/file/MSStream|'''MSStream''']], and an event model to obtain the results of these reads.
'''MSStreamReader''' lets you read and interact with [[apis/file/MSStream|'''MSStream''']] objects.
'''MSStreamReader''' performs the conversion of  multimedia that is in a C++ file format into a format that can be accessed by JavaScript. The original file is accessed as an [[apis/file/MSStream|'''MSStream''']] that overlays an [[apis/file/Blob|'''Blob''']] object.
'''MSStreamReader''' uses the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method to perform an asynchronous read of data from the [[apis/file/MSStream|'''MSStream''']] when converting it to a [[apis/file/Blob|'''Blob''']]. A series of events are used to track the progress of the read and any errors that occur.
The '''MSStreamReader''' can be in one of three states. The [[apis/file/properties/readyState|'''readyState''']] returns the current state. The state is one of the following values:
*EMPTY. The '''MSStreamReader''' object has been created and there are no pending reads. This is the default state of a new '''MSStreamReader'''object, until the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method is called.
*LOADING. 
An [[apis/file/MSStream|'''MSStream''']] is being read. The [[apis/file/methods/readAsBlob|'''readAsBlob''']] method is running and no error has occurred during the read.
*DONE. The entire [[apis/file/MSStream|'''MSStream''']] has been read into memory, a file error occurred during the read, or the read was aborted using the [[apis/file/methods/abort|'''abort''']] method. The '''MSStreamReader''' is no longer reading an '''MSStream'''. If [[apis/file/properties/readyState|'''readyState''']] is set to <code>DONE</code>, it means that the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method has been called at least once.

When the '''MSStreamReader''' read operation is done on the [[apis/file/MSStream|'''MSStream''']], the [[apis/file/properties/result|'''result''']] property returns the [[apis/file/Blob|'''Blob''']] object that contains the data buffered from the '''MSStream'''. The '''result''' is returned after the [[apis/file/events/onloadend|'''onloadend''']] event has fired.
|Import_Notes=
===Syntax===
===Members===
The '''MSStreamReader''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''MSStreamReader''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/file/events/onabort|'''onabort''']]
|Fires when a read or creation operation is aborted by calling the  [[apis/file/methods/abort|'''abort''']] method.
|-
|[[apis/file/events/onerror|'''onerror''']]
|Fires when an error occurs when using the '''msStreamReader''' or [[apis/file/FileReader|'''FileReader''']] object.
|-
|[[apis/file/events/onload|'''onload''']]
|Fires when the creation of, or read by, an '''msStreamReader''' or [[apis/file/FileReader|'''FileReader''']] object successfully completes.
|-
|[[apis/file/events/onloadend|'''onloadend''']]
|Fires when the request to create or read an '''msStreamReader''' or [[apis/file/FileReader|'''FileReader''']] object completes, even if the request fails.
|-
|[[apis/file/events/onloadstart|'''onloadstart''']]
|Fires at the start of  the creation of, or read by, an '''msStreamReader''' or [[apis/file/FileReader|'''FileReader''']] object.
|-
|[[apis/file/events/onprogress|'''onprogress''']]
|Contains a function pointer to the <code>onprogress</code> event handler (callback) function.
|}
 

====Methods====
The '''MSStreamReader''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/file/methods/abort|'''abort''']]
|Aborts a read operation by an [[apis/file/FileReader|'''FileReader''']] object.
|-
|'''readAsArrayBuffer'''
|Reads a '''MSStreamReader''' into memory as an array buffer.
|-
|[[apis/file/methods/readAsBlob|'''readAsBlob''']]
|Performs an asynchronous read of an [[apis/file/MSStream|'''MSStream''']] object in order to create a [[apis/file/Blob|'''Blob''']] object.
|-
|'''readAsDataURL'''
|Reads a '''MSStreamReader''' object into memory as a data URL string.
|-
|[[apis/file/methods/readAsText (MSStreamReader)|'''readAsText''']]
|Reads a '''MSStreamReader''' object into memory as a text string.
|}
 

====Properties====
The '''MSStreamReader''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/file/properties/error|'''error''']]
|The error that occurred while reading the file.
|-
|[[apis/file/properties/readyState|'''readyState''']]
|Contains a constant indicating the current  state of the [[apis/file/FileReader|'''FileReader''']]/'''msStreamReader''' object.
|-
|[[apis/file/properties/result|'''result''']]
|The result of the read operation.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}