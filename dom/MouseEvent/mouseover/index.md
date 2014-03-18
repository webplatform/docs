{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/MouseEvent
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''onmouseover''' event to apply a new style to an object.
|Code=&lt;p 
	onmouseover{{=}}"this.style.color{{=}}'red'" 
    onmouseout{{=}}"this.style.color{{=}}'black'"&gt;
    	Move the mouse pointer over this text to change its color. Move the pointer off the text 
        to change the color back.
&lt;/p&gt;
}}{{Single Example
|Description=This example shows how to change the value of a text area in response to mouse events.
|Code=&lt;p&gt;Move the mouse pointer into the text area to fire the onmouseover event. Move 
it out to clear the text.
&lt;textarea name{{=}}"txtMouseTrack" 
    onmouseover{{=}}"this.value{{=}}'onmouseover fired'" 
    onmouseout{{=}}"this.value{{=}}''"&gt;
&lt;/textarea&gt;&lt;/p&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoverEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The event occurs when the user moves the mouse pointer into the object, and it does not repeat unless the user moves the mouse pointer out of the object and then back into it.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Move the mouse pointer into an object.
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