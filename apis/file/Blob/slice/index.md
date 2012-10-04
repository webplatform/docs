{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=start|Data type=signed long long|Description=The optional start parameter is a value for the start point of a slice call, and is treated as a byte-order position, with position 0 representing the first byte. If start is negative, it is treated as length + start, where length is the length of the file (this allows byte selection starting from the end of the file).|Optional=}}
{{Method Parameter|Name=end|Data type=signed long long|Description=The optional end parameter is a value for the end point of a slice call. The returned ''slice'' of data is up to but does not include the end byte. If end is omitted, '''slice''' selects all bytes from the start position to the end of the file. If end is negative, it is treated as length + end, where length is the length of the file (this allows byte selection starting from the end of the file).|Optional=}}
{{Method Parameter|Name=contentType|Data type=DOMString|Description=The optional contentType parameter is used to set a value (identical to one that is set with the HTTP/1.1 Content-Type header) on the [[apis/file/Blob|'''Blob''']] returned by the slice call.|Optional=}}
{{Method Parameter|Name=retVal|Data type=Blob|Description=|Optional=}}
|Method_applies_to=apis/file/Blob
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The '''slice''' method returns a new [[apis/file/Blob|'''Blob''']] object with bytes ranging from the optional <code>start</code> parameter up to but not including the optional <code>end</code> parameter, and with a type attribute that is the value of the optional <code>contentType</code> parameter.
If it is not possible to obtain the object in the range specified, your application should throw the <code>NotSupportedError</code> exception.
For a code sample of the <code>slice</code> method, see [[apis/file/Blob|'''Blob''']].
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/file/Blob|Blob]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}