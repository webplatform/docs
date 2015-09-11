---
title: drop
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/DragDropEventsEX.htm'
notes:
  - 'Needs summary, specs, and compat'
readiness: 'In Progress'
tags:
  - Events
  - DOM
uri: dom/DragEvent/drop

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

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
## <span>Examples</span>

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

## <span>Notes</span>

### <span>Remarks</span>

The **ondrop** event fires before the [**dragleave**](/dom/DragEvent/dragleave) and [**dragend**](/dom/DragEvent/dragend) events. When scripting custom functionality, use the [**returnValue**](/dom/BeforeUnloadEvent/returnValue) property to disable the default action. You must cancel the default action for [**dragenter**](/dom/DragEvent/dragenter) and [**dragover**](/dom/DragEvent/dragover) in order for **ondrop** to fire. In the case of a **div**, the default action is not to drop. This can be contrasted with the case of an **input type=text** element, where the default action is to drop. In order to allow a drag-and-drop action on a **div**, you must cancel the default action by specifying **window.event.returnValue=false** in both the **ondragenter** and **ondragover** event handlers. Only then will **ondrop** fire. As of Microsoft Internet Explorer 5, drag-and-drop events can be used to carry out drag-and-drop activities, not only with **input type=text** elements, but also with block and inline tags. For example, text can be selected, dragged, then dropped on a **div** target. This causes several target events to fire, including [**dragenter**](/dom/DragEvent/dragenter), [**dragover**](/dom/DragEvent/dragover), and **drop**. Because drag-and-drop actions are not directly supported on block and inline tags, you must use extra scripting to carry out the move or copy to the target using [**innerText**](/dom/HTMLElement/innerText), for example. Calls the associated event handler. To invoke this event, do one of the following:

-   Drag the selection over a valid drop target and release the mouse.

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
