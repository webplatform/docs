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
|Description=This example uses the '''onmouseout''' event to apply a new style to an object.
|Code=&lt;body&gt;
&lt;p onmouseout{{=}}"this.style.color{{=}}'black';" 
    onmouseover{{=}}"this.style.color{{=}}'red';"&gt;
Move the mouse pointer over this text to change its color. 
Move the pointer off the text to change the color back.
&lt;/p&gt;
&lt;/body&gt;
}}{{Single Example
|Description=This example shows how to swap images on mouse events.
|Code=&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function flipImage(url)
{
    if (window.event.srcElement.tagName {{=}}{{=}} "img" )
	{
		window.event.srcElement.src {{=}} url;
    }
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;Move the mouse over the image to see it switch.&lt;/p&gt;
&lt;p&gt;
&lt;img src{{=}}"/workshop/graphics/prop_ro.png" 
    onmouseover{{=}}"flipImage('/workshop/graphics/prop_rw.png');" 
    onmouseout{{=}}"flipImage('/workshop/graphics/prop_ro.png');"&gt;
&lt;/p&gt;
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoutEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
When the user moves the mouse over an object, one [[dom/MouseEvent/mouseover|'''onmouseover''']] event occurs, followed by one or more [[dom/MouseEvent/mousemove|'''onmousemove''']] events as the user moves the mouse pointer within the object. One '''onmouseout''' event occurs when the user moves the mouse pointer out of the object.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Move the mouse pointer out of an object.
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