{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=data|Data type=Sends a string to the server|Description=|Optional=}}
|Method_applies_to=apis/websocket/objects/WebSocket
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=This method does not return a value.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
An ArrayBufferView is a typed array view of an '''ArrayBuffer'''. An '''ArrayBuffer''' is a unformatted block of raw data that is sent in its entirety to a server. By using a typed array to define the format of the buffer, and the start and length (number of elements), you can send portions of an '''ArrayBuffer''' to a server.
This method can throw one of the following exceptions:
{| class="wikitable"
|-
!Exception
!Description
|-
|InvalidStateError(11)
|The connection is not currently OPEN.
|}
 
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>WebSocket</code>
*<code>[[apis/file/methods/readAsBlob|msStreamReader.readAsBlob]]</code>
*<code>[[apis/file/methods/readAsArrayBuffer|FileReader.readAsArrayBuffer]]</code>
*<code>readyState</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}