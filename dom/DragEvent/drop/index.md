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
The '''ondrop''' event fires before the [[dom/DragEvent/dragleave|'''dragleave''']] and [[dom/DragEvent/dragend|'''dragend''']] events.
When scripting custom functionality, use the [[dom/BeforeUnloadEvent/returnValue|'''returnValue''']] property to disable the default action.
You must cancel the default action for [[dom/DragEvent/dragenter|'''dragenter''']] and [[dom/DragEvent/dragover|'''dragover''']] in order for '''ondrop''' to fire. In the case of a '''div''', the default action is not to drop. This can be contrasted with the case of an '''input type{{=}}text''' element, where the default action is to drop.  In order to allow a drag-and-drop action on a '''div''', you must cancel the default action by specifying '''window.event.returnValue{{=}}false''' in both the '''ondragenter''' and '''ondragover''' event handlers. Only then will '''ondrop''' fire.
As of Microsoft Internet Explorer 5, drag-and-drop events can be used to carry out drag-and-drop activities, not only with '''input type{{=}}text''' elements, but also with block and inline tags. For example, text can be selected, dragged, then dropped on a '''div''' target.  This causes several target events to fire, including [[dom/DragEvent/dragenter|'''dragenter''']], [[dom/DragEvent/dragover|'''dragover''']], and '''drop'''.  Because drag-and-drop actions are not directly supported on block and inline tags, you must use extra scripting to carry out the move or copy to the target using [[dom/HTMLElement/innerText|'''innerText''']], for example.
Calls the associated event handler.
To invoke this event, do one of the following:
*Drag the selection over a valid drop target and release the mouse.
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