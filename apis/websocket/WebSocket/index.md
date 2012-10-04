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
{{Notes_Section
|Notes=
===Remarks===
The [http://go.microsoft.com/fwlink/p/?LinkID{{=}}227812 WebSocket] protocol specification defines two URI schemes ws:// and wss:// for unencrypted and encrypted connections, respectively. For example, you could create a new WebSocket connection with the string "ws://example.com:1234/resource". The URL specifies the host to connect to, the port, and (optionally) the protocols you want to use.
'''Note'''  Secure connections (wss://) are recommended in most cases because they are more likely to work with proxy servers, which can buffer unencrypted traffic and close long-lived WebSocket connections without warning.
WebSocket connections are bidirectional; communication can flow in either direction without specific requests and responses. Data can be text or binary.
To open a use a WebSocket connection, you must follow this procedure:
*Create a WebSocket connection with a specific URL and one or more optional subprotocols, such as "chat". You can use the [[apis/websocket/properties/url|'''url''']] property to see how the URL was parsed.
*Determine the state of the connection with the [[apis/websocket/properties/readyState|'''readyState''']] property. This state will change as the communication proceeds.
*Check the type of data that will be sent using the [[apis/websocket/properties/binaryType|'''binaryType''']], [[apis/websocket/properties/protocol|'''protocol''']], and [[apis/websocket/properties/extensions|'''extensions''']] properties.
*Set up  event handlers for the connection. Events include [[apis/websocket/events/onopen|'''onopen''']], [[apis/websocket/events/onmessage|'''onmessage''']], [[apis/websocket/events/onerror|'''onerror''']], and [[apis/websocket/events/onclose|'''onclose''']]. Use [[dom/methods/addEventListener|'''addEventListener''']] to listen for events and [[dom/methods/removeEventListener|'''removeEventListener''']] when you no longer want to listen.
*Send data to the host using the '''send''' method.
*Determine the rate at which your data is moving with the [[apis/websocket/properties/bufferedAmount|'''bufferedAmount''']] property.
*Check to see whether data was sent to you.
*Close the connection when you are finished with the [[apis/websocket/methods/close|'''close''']] method.

 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_websockets\ie]:%20WebSocket object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Syntax===
===Members===
The '''WebSocket''' object has these types of members:
*[#methods Methods]


====Methods====
The '''WebSocket''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|'''close'''
|Closes a WebSocket connection.
|-
|'''send'''
|Sends a string of data to the server.
|-
|[[apis/websocket/methods/send|'''send''']]
|Overloaded. Sends data to the server using a '''WebSocket''' connection.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}