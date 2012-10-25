{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns a new Blob object with bytes ranging from its optional start parameter up to but not including its optional end parameter.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=start
|Data type=Number
|Description=The optional start parameter is a value for the start point of a slice call, and is treated as a byte-order position, with position 0 representing the first byte. If start is negative, it is treated as length + start, where length is the length of the file (this allows byte selection starting from the end of the file).

If you specify a value for start that is larger than the size of the source Blob, the returned Blob has size 0 and contains no data.
|Optional=Yes
}}{{Method Parameter
|Name=end
|Data type=Number
|Description=The optional end parameter is a value for the end point of a slice call. The returned ''slice'' of data is up to but does not include the end byte. If end is omitted, '''slice''' selects all bytes from the start position to the end of the file. If end is negative, it is treated as length + end, where length is the length of the file (this allows byte selection starting from the end of the file).
|Optional=Yes
}}{{Method Parameter
|Name=contentType
|Data type=String
|Description=The optional contentType parameter is used to set a value (identical to one that is set with the HTTP/1.1 Content-Type header) on the [[apis/file/Blob|'''Blob''']] returned by the slice call.
|Optional=Yes
}}
|Method_applies_to=apis/file/Blob
|Example_object_name=blob
|Return_value_name=blob
|Javascript_data_type=Blob
|Return_value_description=A new Blob object containing the data in the specified range of bytes from the source Blob.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''slice''' method returns a new [[apis/file/Blob|'''Blob''']] object with bytes ranging from the optional <code>start</code> parameter up to but not including the optional <code>end</code> parameter, and with a type attribute that is the value of the optional <code>contentType</code> parameter.
If it is not possible to obtain the object in the range specified, your application should throw the <code>NotSupportedError</code> exception.
For a code sample of the <code>slice</code> method, see [[apis/file/Blob|'''Blob''']].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=File API
|URL=http://dev.w3.org/2006/webapi/FileAPI/#dfn-slice
|Status=WD
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
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
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=All
|Version=-
|Note=The slice() method had initially taken length as the second argument to indicate the number of bytes to copy into the new Blob. If you specified values such that start + length exceeded the size of the source Blob, the returned Blob contained data from the start index to the end of the source Blob.
}}
}}
{{See_Also_Section}}
{{Topics|DOM, FileAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}