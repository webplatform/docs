{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The WebSocket object provides the API for creating and managing a WebSocket connection to a server, as well as for sending and receiving data on the connection.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following function can be used to detect WebSocket support.
|Code=function webSocketSupported() {
  return "WebSocket" in window;
}
}}{{Single Example
|Language=JavaScript
|Description=WebSockets are created via the WebSocket() constructor functio
|Code=WebSocket( url[, protocols] )
}}
}}
{{Notes_Section
|Usage=The constructor’s first argument is the URL that the WebSocket will connect to.  When a WebSockets is constructed, it immediately attempts to connect to the given URL.  There is no way to prevent or postpone the connection attempt.  After construction, the WebSocket’s URL is accessible via its “url” property. 
|Notes====Remarks===
[http://dev.w3.org/html5/websockets/ The WebSocket API specification] defines two URI schemes ws:// and wss:// for unencrypted and encrypted connections, respectively. For example, you could create a new WebSocket connection with the string "ws://example.com:1234/resource". The URL specifies the host to connect to, the port, and (optionally) the protocols you want to use.
'''Note'''  Secure connections (wss://) are recommended in most cases because they are more likely to work with proxy servers, which can buffer unencrypted traffic and close long-lived WebSocket connections without warning.
WebSocket connections are bidirectional; communication can flow in either direction without specific requests and responses. Data can be text or binary.
To open a use a WebSocket connection, you must follow this procedure:
*Create a WebSocket connection with a specific URL and one or more optional subprotocols, such as "chat". You can use the [[apis/websocket/properties/url{{!}}'''url''']] property to see how the URL was parsed.
*Determine the state of the connection with the [[apis/websocket/properties/readyState{{!}}'''readyState''']] property. This state will change as the communication proceeds.
*Check the type of data that will be sent using the [[apis/websocket/properties/binaryType{{!}}'''binaryType''']], [[apis/websocket/properties/protocol{{!}}'''protocol''']], and [[apis/websocket/properties/extensions{{!}}'''extensions''']] properties.
*Set up  event handlers for the connection. Events include [[apis/websocket/events/onopen{{!}}'''onopen''']], [[apis/websocket/events/onmessage{{!}}'''onmessage''']], [[apis/websocket/events/onerror{{!}}'''onerror''']], and [[apis/websocket/events/onclose{{!}}'''onclose''']]. Use [[dom/methods/addEventListener{{!}}'''addEventListener''']] to listen for events and [[dom/methods/removeEventListener{{!}}'''removeEventListener''']] when you no longer want to listen.
*Send data to the host using the '''send''' method.
*Determine the rate at which your data is moving with the [[apis/websocket/properties/bufferedAmount{{!}}'''bufferedAmount''']] property.
*Check to see whether data was sent to you.
*Close the connection when you are finished with the [[apis/websocket/methods/close{{!}}'''close''']] method.
|Import_Notes====Syntax===
===Members===
The '''WebSocket''' object has these types of members:
*[[#Methods|Methods]]


====Methods====
The '''WebSocket''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}'''close'''
{{!}}Closes a WebSocket connection.
{{!}}-
{{!}}'''send'''
{{!}}Sends a string of data to the server.
{{!}}-
{{!}}[[apis/websocket/methods/send{{!}}'''send''']]
{{!}}Overloaded. Sends data to the server using a '''WebSocket''' connection.
{{!}}}
 
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
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}