---
title: dragover
tags:
  - Events
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, specs, and compat'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/DragDropEventsEX.htm'
uri: dom/DragEvent/dragover

---
# dragover

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:    ?

## Examples

This example shows when and where each event fires during a drag-and-drop operation by listing each event and the name of the object firing it in a list box.

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

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/DragDropEventsEX.htm)

## Notes

### Remarks

The **dragover** event fires on the target object after the [**dragenter**](/dom/DragEvent/dragenter) event has fired. When scripting custom functionality, use the **returnValue** property to disable the default action. Calls the associated event handler. To invoke this event, do one of the following:

-   Drag the selection over a valid drop target within the client.
-   Drag the selection to a valid drop target within another window.

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

