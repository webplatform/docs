{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires when the user clicks the object with either mouse button or taps the mouse pad.}}
{{Event
|Event_applies_to=dom/MouseEvent
|Synchronous=No
|Bubbles=Yes
|Target=dom/Element
|Cancelable=Yes
|Interface=dom/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to determine the origin of the '''onmousedown''' event when event bubbling is used.
|Code=&lt;BODY onmousedown{{=}}"console.log(event.srcElement.tagName)"&gt;
&lt;TABLE BORDER{{=}}1&gt;
  &lt;TH&gt;Click the items below with your mouse.&lt;/TH&gt;
  &lt;TR&gt;&lt;TD&gt;&lt;BUTTON&gt;Click Me&lt;/BUTTON&gt;&lt;/TD&gt;&lt;/TR&gt;
  &lt;TR&gt;&lt;TD&gt;&lt;INPUT TYPE{{=}}text VALUE{{=}}"Click Me"&gt;&lt;/TD&gt;&lt;/TR&gt;
  &lt;TR&gt;&lt;TD&gt;&lt;SPAN&gt;Click Me&lt;/SPAN&gt;&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;P&gt;This code retrieves the tagName of the object on which
   the onmousedown event has fired.
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousedownEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Use the '''button''' property to determine which mouse button is clicked.
Initiates actions associated with the event and with the object being clicked.
To invoke this event, do one of the following:
*Click a mouse button.
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}