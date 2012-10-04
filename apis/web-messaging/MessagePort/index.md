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
Two '''MessagePort''' objects are automatically created when a [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']] object is created,   and are returned by the [[apis/web-messaging/properties/port1|'''port1''']] and [[apis/web-messaging/properties/port2|'''port2''']] properties.  Messages are sent from one port are received by the other, and vice versa.
The '''MessagePort''' object provides the [[apis/web-messaging/methods/start|'''start''']] method to begin dispatching  messages received on the port, and the [[apis/web-messaging/methods/close|'''close''']] method to close and disconnect the port. The [[apis/web-messaging/methods/postMessage (MessagePort)|'''postMessage''']] method sends  messages through the port.
In Internet Explorer 10, message ports are automatically enabled when a message event is registered with the [[dom/events/message|'''onmessage''']] property or  [[dom/methods/addEventListener|'''addEventListener''']] method. This makes it unnecessary to explicitly call the [[apis/web-messaging/methods/start|'''start''']] method under these conditions.
After posting a '''MessagePort''' object using [[apis/web-messaging/methods/postMessage (MessagePort)|'''postMessage''']], the  '''MessagePort''' object is implicitly [[apis/web-messaging/methods/close|'''closed''']].
For more info, see [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']] for a working messaging demo.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199803 HTML5 Web Messaging]


===Members===
The '''MessagePort''' object has these types of members:
*[#events Events]
*[#methods Methods]


====Events====
The '''MessagePort''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/workers/events/onmessage|'''message''']]
|Returns a message from the parent thread to the worker thread, or between two '''MessagePort''' objects.
|-
|[[dom/events/message|'''onmessage''']]
|Fires when the user sends a cross-document message or a message is sent from a [[apis/workers/objects/Worker|'''Worker''']] with [[apis/web-messaging/methods/postMessage (window)|'''postMessage''']].
|}
 

====Methods====
The '''MessagePort''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/web-messaging/methods/close|'''close''']]
|Closes a '''MessagePort''' from an existing [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']].
|-
|[[apis/web-messaging/methods/postMessage (MessagePort)|'''postMessage''']]
|Sends messages between two connected '''MessagePorts''' in a [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']].
|-
|[[apis/web-messaging/methods/start|'''start''']]
|Allows the '''MessagePort''' to begin receiving messages.
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