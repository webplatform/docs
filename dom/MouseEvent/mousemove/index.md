{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires when the user moves the mouse over the object. }}
{{Event
|Event_applies_to=dom/MouseEvent
|Synchronous=No
|Bubbles=Yes
|Target=dom/Element
|Cancelable=No
|Interface=dom/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''onmousemove''' event to monitor the location of the mouse cursor on the screen. When the mouse cursor moves over the '''div''' object, a '''span''' object is updated with the [[dom/MouseEvent/clientX|'''clientX''']] and [[dom/MouseEvent/clientY|'''clientY''']] property values. The '''clientX''' and '''clientY''' properties are exposed by the event object.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function fnTrackMouse(){
   oNotice.innerText{{=}}"Coords: (" + event.clientX + ", 
      " + event.clientY + ")";
}
&lt;/script&gt;
&lt;div id{{=}}"oScratch" onmousemove{{=}}"fnTrackMouse()"&gt;
  &lt;span id{{=}}"oNotice"&gt;&lt;/span&gt;
&lt;/div&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousemoveEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
If the user presses a mouse button, use the '''button''' property to determine which button was pressed.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Move the mouse over the document.
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}