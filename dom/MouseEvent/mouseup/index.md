{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires when the user releases a mouse button while the mouse is over the object.}}
{{Event
|Event_applies_to=dom/MouseEvent
|Synchronous=No
|Bubbles=Yes
|Target=dom/Element
|Cancelable=Yes
|Default_action=Invoke a context menu (in combination with the right mouse button, if supported)
|Interface=dom/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Use the '''button''' property to determine which mouse button is pressed.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Press and release a mouse button.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN, HTML5Rocks
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/Events/mouseup mouseup event]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536950(v=vs.85).aspx mouseup event]
|HTML5Rocks_link=[http://www.html5rocks.com/en/search?q=mouseup+event mouseup event samples]
}}