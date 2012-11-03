{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The '''Blob''' object represents immutable raw data. It provides a method to slice data objects between ranges of bytes into further chunks of raw data.}}
{{API_Object
|Overview="Blob" provides an attribute representing the size of the chunk of data. The [[apis/file/File|'''File''']] object inherits from the '''Blob''' object.
'''Blob''' objects can be read asynchronously only on the main thread via [[apis/file/FileReader|'''FileReader''']] 
objects, but metadata access via attributes such as '''size''' and '''type''' return 
synchronously (this trade-off is based on the underlying assumption that metadata access will not significantly block or disrupt the browser's main thread, whereas 
reading '''Blob''' data will).
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=var aFileParts = ["<a id=\"a\"><b id=\"b\">hey!<\/b><\/a>"];
var oMyBlob = new Blob(aFileParts, { "type" : "text\/xml" }); // the blob
}}
}}
{{Notes_Section
|Import_Notes=====Methods====
The '''Blob''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[apis/file/methods/close{{!}}'''close''']]
{{!}}Releases the file lock for the associated file  resource or frees the memory for the '''Blob''' object. After calling this method, performing addition operations on the '''Blob''' object fails and throws an exception.
{{!}}-
{{!}}[[apis/file/methods/slice{{!}}'''slice''']]
{{!}}Returns a new '''Blob''' object with bytes ranging from its optional <code>start</code> parameter up to but not including its optional <code>end</code> parameter.
{{!}}}
 

====Properties====
The '''Blob''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}'''msRandomAccessStream'''
{{!}}Provides access to an IRandomAccessStream object.
{{!}}-
{{!}}[[apis/file/properties/size{{!}}'''size''']]
{{!}}The size of the '''Blob''' object in bytes.
{{!}}-
{{!}}[[apis/file/properties/type{{!}}'''type''']]
{{!}}Returns the content type of the object.
{{!}}}
 
 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=File API Specification: Blob
|URL=http://dev.w3.org/2006/webapi/FileAPI/#dfn-Blob
|Status=WD
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=5
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=slice()
|Chrome_supported=Yes
|Chrome_version=21
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=10
|Firefox_supported=Yes
|Firefox_version=13
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=5
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Blob() constructor
|Chrome_supported=Yes
|Chrome_version=20
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=13.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=6
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Basic Support
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=13.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM, FileAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/Blob
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}