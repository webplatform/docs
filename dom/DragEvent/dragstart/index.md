---
title: dragstart
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ondragstartEX.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/DragDropEventsEX.htm'
notes:
  - 'Needs summary, specs, and compat'
readiness: 'In Progress'
tags:
  - Events
  - DOM
uri: dom/DragEvent/dragstart

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
 ?

</td>
</tr>
</table>
## Examples

This example uses event bubbling to handle the **ondragstart** event at the **body** level.

``` html
<body ondragstart="console.log(event.srcElement.tagName)">
    <input type="text" value="Select and drag this text">
    Select and drag this text
    <textarea>Select and drag this text</textarea>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ondragstartEX.htm)

This example shows when and where each event fires during a drag-and-drop operation by listing each event and the name of the object firing it in a list box.

``` html
<HEAD>
<SCRIPT>
// Code for dynamically adding options to a select.
function ShowResults()
{               // Information about the events
                 // and what object fired them.
  arg = event.type + "  fired by  " + event.srcElement.id;
  var oNewOption = new Option();
  oNewOption.text = arg;
  oResults.add(oNewOption,0);
}
</SCRIPT>
</HEAD>
<BODY>
<P>Source events are wired up to this text box.</P>
<INPUT ID=txtDragOrigin VALUE="Text to Drag"
    ondragstart="ShowResults()"
    ondrag="ShowResults()"
    ondragend="ShowResults()"
>
<P>Target events are bound to this text box.</P>
<INPUT ID=txtDragDestination VALUE="Drag Destination"
    ondragenter="ShowResults()"
    ondragover="ShowResults()"
    ondragleave="ShowResults()"
    ondrop="ShowResults()"
>
<SELECT ID=oResults SIZE=30>
  <OPTION>List of Events Fired
</SELECT>
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/DragDropEventsEX.htm)

## Notes

### Remarks

The **ondragstart** event is the first to fire when the user starts to drag the mouse. It is essential to every drag operation, yet is just one of several source events in the data transfer object model. Source events use the [**setData**](/dom/DataTransfer/setData) method of the [**dataTransfer**](/dom/DataTransfer) object to provide information about data being transferred. Source events include **dragstart**, [**drag**](/dom/DragEvent/drag), and [**dragend**](/dom/DragEvent/dragend). When dragging anything other than an **img** object, some text to be dragged must be selected. Calls the associated event handler. To invoke this event, do one of the following:

-   Drag the selected text or object.

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
