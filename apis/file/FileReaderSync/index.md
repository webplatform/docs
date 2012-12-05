{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Allows for synchronous reading of '''File''' or '''Blob''' objects. Only available in [[apis/workers/objects/Worker|Workers]], since synchronous I/O would otherwise block the main application from executing.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
'''Important'''  The '''FileReaderSync''' object's read methods ([[apis/file/methods/readAsText (File and Blob)|'''readAsText''']], [[apis/file/methods/readAsDataURL|'''readAsDataURL''']], and [[apis/file/methods/readAsArrayBuffer|'''readAsArrayBuffer''']]) have the same method signatures as the read methods of the [[apis/file/FileReader|'''FileReader''']] object but they behave synchronously (as opposed to asynchronously).
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_fileapi\ie]:%20FileReaderSync object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes====Syntax===
===Members===
The '''FileReaderSync''' object has these types of members:
*[#methods Methods]


====Methods====
The '''FileReaderSync''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
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
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/FileReaderSync
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}