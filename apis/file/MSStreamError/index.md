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
{{Notes_Section
|Notes=
===Remarks===
The [[apis/file/MSStream|'''msStream''']] object's <code>error</code> property is an 
'''MSStreamError''' object and is accessed asynchronously through the 
<code>onerror</code> event handler when error events are generated. The 
'''MSStreamError''' object's [[apis/file/properties/code|'''code''']] property and associated error codes allow asynchronous file error handling.
|Import_Notes=
===Syntax===
===Members===
The '''MSStreamError''' object has these types of members:
*[#properties Properties]


====Properties====
The '''MSStreamError''' object has these properties.
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
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/file/FileError|FileError]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}