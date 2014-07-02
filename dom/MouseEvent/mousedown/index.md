{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=Yes
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
|Code=&lt;body onmousedown{{=}}"(event.target)?alert(event.target.tagName):alert(event.srcElement.tagName);"&gt;
&lt;table style{{=}}"table-layout:fixed; cell-collapse:collapse"&gt;
&lt;tr&gt;
  &lt;th&gt;Click the items below with your mouse.&lt;/th&gt;
&lt;/tr&gt;
  &lt;tr&gt;&lt;td&gt;&lt;button type{{=}}"button"&gt;Click Me&lt;/button&gt;&lt;/td&gt;&lt;/tr&gt;
  &lt;tr&gt;&lt;td&gt;&lt;input type{{=}}"text" value{{=}}"Click Me"/&gt;&lt;/td&gt;&lt;/tr&gt;
  &lt;tr&gt;&lt;td&gt;&lt;span&gt;Click Me&lt;/span&gt;&lt;/td&gt;&lt;/tr&gt;
&lt;/table&gt;
&lt;p&gt;This code retrieves the tagName of the object on which
   the onmousedown event has fired.&lt;/p&gt;
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousedownEX.htm
}}
}}
{{Notes_Section
|Usage=Determine the properties of the DOM element that a user clicks on.
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/Events/mousedown mousedown]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536944(v=vs.85).aspx event.mousedown]
|HTML5Rocks_link=
}}