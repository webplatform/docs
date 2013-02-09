{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Transmits data to the server over the WebSocket connection.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=data
|Data type=any
|Optional=No
}}
|Method_applies_to=apis/websocket/objects/WebSocket
|Example_object_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var data = new ArrayBuffer(10000000);

// perform some operations on the ArrayBuffer
socket.send(data);

if (socket.bufferedAmount === 0) {
  // the data sent
}
else {
  // the data did not send
}
}}
}}
{{Notes_Section
|Notes====Remarks===
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
 
|Import_Notes====Syntax===
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>WebSocket</code>
*<code>[[apis/file/methods/readAsBlob|msStreamReader.readAsBlob]]</code>
*<code>[[apis/file/methods/readAsArrayBuffer|FileReader.readAsArrayBuffer]]</code>
*<code>readyState</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}