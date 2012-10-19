{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/DragEvent
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows when and where each event fires during a drag-and-drop operation by listing each event and the name of the object firing it in a list box.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/DragDropEventsEX.htm
|Code=
&lt;HEAD&gt;
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
This event fires on the source object after the  event. The '''ondrag''' event fires throughout the drag operation, whether the selection being dragged is over the drag source, a valid target, or an invalid target.
Calls the associated event handler if there is one.
To invoke this event, do one of the following:
*Drag a text selection or object within the client.
*Drag a text selection or object to another client.
*Drag a text selection or object to a drop target in another application.
*Drag a text selection or object to the system desktop.

|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>area</code>
*<code>audio</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>[[canvas/objects/canvas|canvas]]</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>[[dom/document|document]]</code>
*<code>dt</code>
*<code>em</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>hn</code>
*<code>hr</code>
*<code>i</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>kbd</code>
*<code>label</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>[[html/elements/media|media]]</code>
*<code>menu</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>s</code>
*<code>samp</code>
*<code>small</code>
*<code>source</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>video</code>
*<code>window</code>
*<code>xmp</code>
*<code>About DHTML Data Transfer</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}