{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
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
When the <code>FileReader</code> constructor is invoked, a new '''FileReader''' object is returned. 
This '''FileReader''' object enables asynchronous reads on individual [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] objects by firing progress events as the read occurs to event handler methods attached to the '''FileReader''' object.
|Import_Notes=
===Syntax===
===Members===
The '''FileReader''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''FileReader''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/file/events/onabort|'''onabort''']]
|Fires when a read or creation operation is aborted by calling the  [[apis/file/methods/abort|'''abort''']] method.
|-
|[[apis/file/events/onerror|'''onerror''']]
|Fires when an error occurs when using the [[apis/file/MSStreamReader|'''msStreamReader''']] or '''FileReader''' object.
|-
|[[apis/file/events/onload|'''onload''']]
|Fires when the creation of, or read by, an [[apis/file/MSStreamReader|'''msStreamReader''']] or '''FileReader''' object successfully completes.
|-
|[[apis/file/events/onloadend|'''onloadend''']]
|Fires when the request to create or read an [[apis/file/MSStreamReader|'''msStreamReader''']] or '''FileReader''' object completes, even if the request fails.
|-
|[[apis/file/events/onloadstart|'''onloadstart''']]
|Fires at the start of  the creation of, or read by, an [[apis/file/MSStreamReader|'''msStreamReader''']] or '''FileReader''' object.
|-
|[[apis/file/events/onprogress|'''onprogress''']]
|Contains a function pointer to the <code>onprogress</code> event handler (callback) function.
|}
 

====Methods====
The '''FileReader''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/file/methods/abort|'''abort''']]
|Aborts a read operation by an '''MSStreamReader''' or '''FileReader''' object.
|-
|[[apis/file/methods/readAsArrayBuffer|'''readAsArrayBuffer''']]
|Reads a [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] into memory as an array buffer.
|-
|[[apis/file/methods/readAsDataURL|'''readAsDataURL''']]
|Reads a [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] into memory as a data URL string.
|-
|[[apis/file/methods/readAsText (File and Blob)|'''readAsText''']]
|Reads a [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] into memory as a text string.
|}
 

====Properties====
The '''FileReader''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/file/properties/error|'''error''']]
|The error that occurred while reading the file.
|-
|[[apis/file/properties/readyState|'''readyState''']]
|Contains a constant indicating the current  state of the '''FileReader'''/[[apis/file/MSStreamReader|'''msStreamReader''']] object.
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