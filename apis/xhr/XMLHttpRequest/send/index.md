{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=varBody|Data type=any|Description=Any that specifies the body of the message being sent with the request.|Optional=}}
|Method_applies_to=apis/xhr/objects/XMLHttpRequest
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=This method does not return a value.

This method does not return a value.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
'''send''' was introduced in Windows Internet Explorer 7.
This method is synchronous or asynchronous, depending on the value of the ''varAsync'' parameter in the '''open''' method call. If synchronous, this call does not return until the entire response is received or the protocol stack time out period expires. If asynchronous, this call returns immediately.
This optional ''varBody'' parameter may be a '''String''', '''array''' of unsigned bytes, or  an XML Document Object Model (DOM) object. For additional information, see send Method (IXMLHTTPRequest).
'''Warning'''  It is now possible to use '''XMLHttpRequest''' to upload extremely large objects, such as [[apis/file/Blob|'''Blob''']] objects and [[dom/FormData|'''FormData''']] objects, which may take a long time to complete. Because Metro style apps using JavaScript can be terminated at any time, there is a risk the upload will not complete.  Consider using the Windows Runtime file upload APIs, such as [http://go.microsoft.com/fwlink/p/?LinkId{{=}}254693 BackgroundTransfer],  for these operations. For more information, see [http://go.microsoft.com/fwlink/p/?LinkId{{=}}254692 Quickstart: Uploading a file].
An ArrayBufferView is a typed array view of an ArrayBuffer. Introduced in Internet Explorer 10, an ArrayBuffer is a unformatted block of raw data that is sent in its entirety to a server. By using a typed array to define the format of the buffer, and the start and length (number of elements), you can send portions of an ArrayBuffer to a server.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3.6.3
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 4.7.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>XMLHttpRequest</code>
*<code>Reference</code>
*<code>open</code>
*<code>setRequestHeader</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}