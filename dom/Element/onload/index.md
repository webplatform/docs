{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Interface=apis/file/MSStream
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Notes_Section
|Notes=
===Remarks===
This event fires when the [[apis/file/MSStreamReader|'''msStreamReader''']] is successfully created or when the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method finishes the read of a [[apis/file/Blob|'''Blob''']] or [[apis/file/MSStream|'''msStream''']] object. If the operation fails, [[dom/events/load|'''onload''']] does not fire, but instead, the [[apis/file/events/onloadend|'''onloadend''']] event and '''onerror''' events fire.
Creates or loads an [[apis/file/MSStreamReader|'''msStreamReader''']] object.
To invoke this event, do one of the following:
*Create an [[apis/file/MSStreamReader|'''msStreamReader''']] object.
*Invoke the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method.

The ''pEvtObj'' parameter is required for the following interfaces:
*[[apis/file/MSStreamReader|'''msStreamReader''']]

|Import_Notes=
===Syntax===
===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/file/FileReader|FileReader]]</code>
*<code>[[apis/file/MSStreamReader|msStreamReader]]</code>
*<code>[[dom/methods/click|click]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}