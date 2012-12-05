{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''FileReader''' object lets web applications asynchronously read the contents of files (or raw data buffers) stored on the user's computer, using [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] objects to specify the file or data to read. [[apis/file/File|'''File''']] objects may be obtained from a [[apis/file/FileList|'''FileList''']] object returned as a result of a user selecting files using the [[input]] element, from a drag-and-drop operation's [[DataTransfer]] object, or from the [[mozGetAsFile() API]] on an [[HTMLCanvasElement]].}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
When the <code>FileReader</code> constructor is invoked, a new '''FileReader''' object is returned. 
This '''FileReader''' object enables asynchronous reads on individual [[apis/file/File|'''File''']] or [[apis/file/Blob|'''Blob''']] objects by firing progress events as the read occurs to event handler methods attached to the '''FileReader''' object.
|Import_Notes====Syntax===
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
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=6.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.6
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=6.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=3.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=10.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.5
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=6.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer Mobile
|Version=10.0
|Note=The feature is implemented, however, disabled.
}}
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/FileReader
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}