{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, specs, and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/DragEvent
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/DragEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows when and where each event fires during a drag-and-drop operation by listing each event and the name of the object firing it in a list box.
|Code=&lt;HEAD&gt;
&lt;SCRIPT&gt;
// Code for dynamically adding options to a select.
function ShowResults()
{				// Information about the events 
				 // and what object fired them.
  arg {{=}} event.type + "  fired by  " + event.srcElement.id;  
  var oNewOption {{=}} new Option(); 
  oNewOption.text {{=}} arg;
  oResults.add(oNewOption,0);
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P&gt;Source events are wired up to this text box.&lt;/P&gt;
&lt;INPUT ID{{=}}txtDragOrigin VALUE{{=}}"Text to Drag"
    ondragstart{{=}}"ShowResults()"
    ondrag{{=}}"ShowResults()"
    ondragend{{=}}"ShowResults()"
&gt;
&lt;P&gt;Target events are bound to this text box.&lt;/P&gt;
&lt;INPUT ID{{=}}txtDragDestination VALUE{{=}}"Drag Destination"
    ondragenter{{=}}"ShowResults()"
    ondragover{{=}}"ShowResults()"
    ondragleave{{=}}"ShowResults()"
    ondrop{{=}}"ShowResults()"
&gt;
&lt;SELECT ID{{=}}oResults SIZE{{=}}30&gt;
  &lt;OPTION&gt;List of Events Fired
&lt;/SELECT&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/DragDropEventsEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''ondragleave''' event does not support the '''Event''' object's '''toElement''' and '''fromElement''' properties.
Calls the associated event handler.
To invoke this event, do one of the following:
*Drag the selection over a valid drop target, and then move that selection out again without dropping it.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

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