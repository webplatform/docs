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
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
When you create a new '''MessageChannel''' object, it has two connected [[apis/web-messaging/objects/MessagePort|'''MessagePort''']] objects ([[apis/web-messaging/properties/port1|'''port1''']] and [[apis/web-messaging/properties/port2|'''port2''']]).   One of the ports is sent to another window or frame, and messages can be sent and received without repeated origin checking that is needed when using [[apis/web-messaging/methods/postMessage (window)|'''window.postMessage''']]. Validation of the origin of a port and messages need only be done when a port is sent to windows other than the one that created them.  '''MessagePort''' simplifies the messaging process by sending and receiving messages through two (and only those two) connected ports.
Messages are posted between the ports using [[apis/web-messaging/methods/postMessage (MessagePort)|'''postMessage''']]. Since the ports will only accept messages between the connected ports, no  further validation is required once the connection is established. '''MessageChannel''' enables asynchronous communication between [[dom/HTMLIFrameElement|'''IFrameElements''']], cross-domain windows, or same page communications.
The following example shows how a  parent window can communicate directly with a worker thread that is inside an iframe by using  a '''MessageChannel'''.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199803 HTML5 Web Messaging]


===Members===
The '''MessageChannel''' object has these types of members:
*[#properties Properties]


====Properties====
The '''MessageChannel''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/web-messaging/properties/port1|'''port1''']]
|Returns the first [[apis/web-messaging/methods/start|'''MessagePort''']] object of a '''MessageChannel''' object.
|-
|[[apis/web-messaging/properties/port2|'''port2''']]
|Returns the second [[apis/web-messaging/methods/start|'''MessagePort''']] object  of a '''MessageChannel''' object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/workers/objects/Worker|Worker]]</code>
*<code>[http://go.microsoft.com/fwlink/?LinkID{{=}}254465 Web worker demo]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}