{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The File object provides information about -- and access to the contents of -- files. These are generally retrieved from a FileList object returned as a result of a user selecting files using the input element, or from a drag and drop operation's DataTransfer object.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
===Members===
The '''File''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''File''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/file/methods/msClose|'''msClose''']]
|Releases the file lock for the associated file  resource or frees the memory for the [[apis/file/Blob|'''Blob''']] object. After calling this method, performing addition operations on the '''Blob''' object fails and throws an exception.
|}
 

====Properties====
The '''File''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/file/properties/lastModifiedDate|'''lastModifiedDate''']]
|The last modified date of the file.
|-
|[[apis/file/properties/name|'''name''']]
|The name of the file.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
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