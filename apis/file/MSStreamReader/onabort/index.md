{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Non-standard; deletion candidate
|Checked_Out=No
|High-level issues=Deletion Candidate, Needs Review
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Indicates that the read has been aborted (for example, by calling '''abort()''').}}
{{API_Object_Property
|Property_applies_to=apis/file/MSStreamReader
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
|Event_applies_to=dom/Element
|Interface=apis/file/MSStream
|Target=dom/Element
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Aborts a read by, or a creation of, an [[apis/file/MSStreamReader|'''msStreamReader''']] object.
To invoke this event, do one of the following:
*Abort the creation of  an [[apis/file/MSStreamReader|'''msStreamReader''']] object.
*Invoke the [[apis/file/methods/abort|'''abort''']] method.

The ''pEvtObj'' parameter is required for the following interfaces:
*[[apis/file/MSStreamReader|'''msStreamReader''']]
|Import_Notes====Syntax===
===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/file/FileReader|FileReader]]</code>
*<code>[[apis/file/MSStreamReader|msStreamReader]]</code>
*<code>[[dom/methods/click|click]]</code>
}}
{{Topics|API, FileAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}



{{Editorial/Deletion_Candidate|MS proprietary}}