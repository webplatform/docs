{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/objects/Event
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
'''CloseEvent''' is sent to clients using [[apis/websocket/objects/WebSocket|'''WebSockets''']] when the connection is closed. This is delivered to the listener indicated by the WebSocket object's [[apis/websocket/events/onclose|'''onclose''']] attribute.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_dom_events\ie]:%20CloseEvent object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Members===
The '''CloseEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''CloseEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/initCloseEvent|'''initCloseEvent''']]
|Initializes the close event.
|}
 

====Properties====
The '''CloseEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/code|'''code''']]
|The  connection close-code provided by the server.
|-
|[[dom/properties/reason|'''reason''']]
|Server close-connection reason.
|-
|[[dom/properties/wasClean|'''wasClean''']]
|Indicates whether the server connection closed cleanly.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}