---
title: offline
tags:
  - Events
readiness: 'In Progress'
notes:
  - 'Needs summary, spec, and compat'
uri: dom/Element/offline

---
# offline

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
:

## Examples

The following example sets an event handler that responds to both [**ononline**](/dom/Element/online) and **onoffline** events using the **type** property of the **event** object.

    function reportConnectionEvent(e)
    {
        if (!e) e = window.event;

        if ('online' == e.type) {
            alert( 'The browser is ONLINE.' );
        }
        else if ('offline' == e.type) {
            alert( 'The browser is OFFLINE.' );
        }
        else {
            alert( 'Unexpected event: ' + e.type );
        }
    }
    window.onload = function() {
        document.body.ononline = reportConnectionEvent;
        document.body.onoffline = reportConnectionEvent;
    }

## Notes

### Remarks

If Asynchronous JavaScript and XML (AJAX) Connection Services are disabled, this event is not raised. (These services are enabled by default.) To invoke this event, do one of the following:

-   Set the browser to "Work Offline" on the **File** menu.

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages (MSDN)

-   `body`
-   `frameSet`
-   `Window`
-   `Reference`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

