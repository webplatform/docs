{{Page_Title}}
{{Flags}}
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
|Example_object_name=Blob
|Javascript_data_type=Blob
|Return_value_description=A new Blob object containing the data in the specified range of bytes from the source Blob.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The '''slice''' method returns a new [[apis/file/Blob|'''Blob''']] object with bytes ranging from the optional <code>start</code> parameter up to but not including the optional <code>end</code> parameter, and with a type attribute that is the value of the optional <code>contentType</code> parameter.
If it is not possible to obtain the object in the range specified, your application should throw the <code>NotSupportedError</code> exception.
For a code sample of the <code>slice</code> method, see [[apis/file/Blob|'''Blob''']].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5 Specification
|URL=http://www.w3.org/TR/FileAPI#blob
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=6.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Basic Support
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=3.0
|Blackberry_supported=Yes
|Blackberry_version=10.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
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
|Browser=All
|Version=-
|Note=The slice() method had initially taken length as the second argument to indicate the number of bytes to copy into the new Blob. If you specified values such that start + length exceeded the size of the source Blob, the returned Blob contained data from the start index to the end of the source Blob.
}}
}}
{{See_Also_Section}}
{{Topics|FileAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}