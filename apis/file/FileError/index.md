{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Represents an error that occurs while using the FileReader interface. Obsolete per latest specification. Use DOMError instead.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The [[apis/file/FileReader|'''FileReader''']] object's <code>error</code> property is a 
'''FileError''' object and is accessed asynchronously through the 
<code>onerror</code> event handler when error events are generated. The 
'''FileError''' object's [[apis/file/properties/code|'''code''']] property and associated error codes allow asynchronous file error handling, as suggested in the following example.
'''Note'''  Errors in the synchronous read methods for Web Workers are reported in the same way.
|Import_Notes====Syntax===
===Members===
The '''FileError''' object has these types of members:
*[#properties Properties]


====Properties====
The '''FileError''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/file/properties/code|'''code''']]
|'''Note'''  
Internet Explorer 10. This object was supported in pre-release versions of Internet Explorer 10. As of Internet Explorer 10,
it is obsolete and  [[dom/DOMError|'''DOMError''']] should be used instead. Applications using this object should be updated 
accordingly.
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
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/FileError
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}