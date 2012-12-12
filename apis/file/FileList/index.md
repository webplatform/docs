{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|FileList is an object which represents an array of individually selected files from the underlying system. |FileList is an object which represents an array of individually selected files from the underlying system_ The user interface for selection can be invoked via <code><input type="file"></code>.
|An object of this type is returned by the files property of the HTML input element; this lets you access the list of files selected with the <input type="file"> element. It's also used for a list of files dropped into web content when using the drag and drop API; see the DataTransfer object for details on this usage.
}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
===Members===
The '''FileList''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''FileList''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/file/methods/item|'''item''']]
|Returns a [[apis/file/File|''' File''']] object from a '''FileList'''.
|}
 

====Properties====
The '''FileList''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/file/properties/length|'''length''']]
|Returns the number of files contained in a '''file list'''.
|}
 
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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/FileList
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}