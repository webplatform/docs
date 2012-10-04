{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=msg|Data type=One of the following:|Description=JavaScript primitive, such as a string

'''object'''

Array

[[canvas/objects/CanvasPixelArray|'''PixelArray''']] object

[[canvas/objects/CanvasImageData|'''ImageData''']] object

[[apis/file/Blob|'''Blob''']]


[[apis/file/File|'''File''']]

ArrayBuffer|Optional=}}
{{Method Parameter|Name=ports|Data type=MessagePort|Description=|Optional=}}
|Method_applies_to=apis/web-messaging/objects/MessagePort
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=This method does not return a value.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
When you create a new [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']] object, it has two connected [[apis/web-messaging/objects/MessagePort|'''MessagePort''']] objects that can only send and receive messages between them.  If the ''ports'' parameter is supplied but contains errors, an '''InvalidStateError''' exception is thrown. Sending a message containing an un-supported object (such as a function), a '''DataCloneError''' exception is thrown.
For more info, see [[apis/web-messaging/objects/MessageChannel|'''MessageChannel''']] for a working messaging demo.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199803 HTML5 Web Messaging]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/web-messaging/objects/MessagePort|MessagePort]]</code>
*<code>[[apis/workers/objects/Worker|Worker]]</code>
*<code>[[apis/web-messaging/objects/MessageChannel|MessageChannel]]</code>
*<code>[http://go.microsoft.com/fwlink/?LinkID{{=}}254465 Web worker demo]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}