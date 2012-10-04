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
The '''Blob''' object represents immutable raw data. It provides a method to slice data objects between ranges of bytes into further chunks of raw data. It also 
provides an attribute representing the size of the chunk of data. The [[apis/file/File|'''File''']] object inherits from the '''Blob''' object.
'''Blob''' objects can be read asynchronously only on the main thread via [[apis/file/FileReader|'''FileReader''']] 
objects, but metadata access via attributes such as '''size''' and '''type''' return 
synchronously (this trade-off is based on the underlying assumption that metadata access will not significantly block or disrupt the browser's main thread, whereas 
reading '''Blob''' data will).
|Import_Notes=
===Syntax===
===Members===
The '''Blob''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''Blob''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/file/methods/msClose|'''msClose''']]
|Releases the file lock for the associated file  resource or frees the memory for the '''Blob''' object. After calling this method, performing addition operations on the '''Blob''' object fails and throws an exception.
|-
|[[apis/file/methods/slice|'''slice''']]
|Returns a new '''Blob''' object with bytes ranging from its optional <code>start</code> parameter up to but not including its optional <code>end</code> parameter.
|}
 

====Properties====
The '''Blob''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|'''msRandomAccessStream'''
|Provides access to an IRandomAccessStream object.
|-
|[[apis/file/properties/size|'''size''']]
|The size of the '''Blob''' object in bytes.
|-
|[[apis/file/properties/type|'''type''']]
|Returns the content type of the object.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}