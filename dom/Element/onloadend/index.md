{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Interface=dom/objects/Event
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
This event is dispatched when the load ends due to an error or the load ends successfully. It occurs only one time.
Indicates that the requested action is complete.
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