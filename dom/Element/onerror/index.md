{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=apis/file/MSStream
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Event}}
{{Notes_Section
|Notes=
===Remarks===
This event fires when an error occurs during the creation of an [[apis/file/MSStreamReader|'''msStreamReader''']] or a read by the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method. When an error occurs, the operation is stopped, the [[apis/file/events/onloadend|'''onloadend''']] event fires, and the error is passed by the [[apis/file/properties/error|'''error''']] property.
Displays the error message when a problem occurs and executes any error handling routine associated with the event.
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