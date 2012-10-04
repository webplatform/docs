{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Page_Title|web-messaging reference}}
{{Basic_Page}}
{{Notes_Section
|Import_Notes=
===In this section===
{| class="wikitable"
|-
!Topic
!Description
|-
|[[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']]
|Provides a two way  asynchronous messaging through two related ports enabling intra, and inter-window communication.
|-
|[[apis/web-messaging/objects/MessagePort|'''MessagePort''']]
|Provides an object where messages can be sent and received through a [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']].
|-
|[[apis/web-messaging/methods/close|'''close''']]
|Closes a [[apis/web-messaging/objects/MessagePort|'''MessagePort''']] from an existing [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']].
|-
|[[apis/web-messaging/methods/postMessage (MessagePort)|'''postMessage (MessagePort)''']]
|Sends messages between two connected [[apis/web-messaging/objects/MessagePort|'''MessagePorts''']] in a [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']].
|-
|[[apis/web-messaging/methods/postMessage (window)|'''postMessage (window)''']]
|Sends a cross-document message.
|-
|[[apis/web-messaging/methods/start|'''start''']]
|Allows the [[apis/web-messaging/objects/MessagePort|'''MessagePort''']] to begin receiving messages.
|-
|[[apis/web-messaging/properties/port1|'''port1''']]
|Returns the first [[apis/web-messaging/methods/start|'''MessagePort''']] object of a [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']] object.
|-
|[[apis/web-messaging/properties/port2|'''port2''']]
|Returns the second [[apis/web-messaging/methods/start|'''MessagePort''']] object  of a [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']] object.
|}
 

 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_messaging\ie]:%20HTML5 Web Messaging%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}