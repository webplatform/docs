{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=No
|Interface=dom/objects/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This event is dispatched when the load ends due to an error or the load ends successfully. It occurs only one time.
Indicates that the requested action is complete.
To invoke this event, do one of the following:
*Create an [[apis/file/MSStreamReader|'''msStreamReader''']] object.
*Invoke the [[apis/file/methods/readAsBlob|'''readAsBlob''']] method.

The ''pEvtObj'' parameter is required for the following interfaces:
*[[apis/file/MSStreamReader|'''msStreamReader''']]
|Import_Notes====Syntax===
===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/file/FileReader|FileReader]]</code>
*<code>[[apis/file/MSStreamReader|msStreamReader]]</code>
*<code>[[dom/methods/click|click]]</code>
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}