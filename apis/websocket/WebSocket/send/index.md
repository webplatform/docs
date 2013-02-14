{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Transmits data to the server over the WebSocket connection.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=data
|Data type=any
|Description=Must be of one of the following types:
*String
*Blob
*ArrayBuffer
*ArrayBufferView
|Optional=No
}}
|Method_applies_to=apis/websocket/WebSocket
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
|Notes=An '''ArrayBuffer''' is a unformatted block of raw data that is sent in its entirety to a server. An ArrayBufferView is a typed array view of an '''ArrayBuffer'''. By using a typed array to define the format of the buffer, and the start and length (number of elements), you can send portions of an '''ArrayBuffer''' to a server.
This method can throw one of the following exceptions:
{{{!}} class="wikitable"
{{!}}-
!Exception
!Description
{{!}}-
{{!}}InvalidStateError(11)
{{!}}The connection is not currently OPEN.
{{!}}}
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C WebSocket Specification
|URL=http://www.w3.org/TR/websockets/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|WebSocket}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}