---
title: storage
tags:
  - Events
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs summary, examples, compat, better spec link'
uri: dom/Document/storage

---
# storage

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

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The [**URL**](/dom/Window/URL) property specifies the URL of the Web page that made the update. For Windows Internet Explorer 9 standards mode, **onstorage** will only fire on window objects. Handlers attached to document.body or document objects will not receive the event. (Note this does not apply to the [**storagecommit**](/dom/Document/storagecommit) event.) The **onstorage** event will only fire on window objects. Handlers attached to document.body or document objects will not receive the event. (Note this does not apply to the [**storagecommit**](/dom/Document/storagecommit) event.) The **onstorage** event is specified in the W3C [Web Storage](http://go.microsoft.com/fwlink/?LinkId=217507) specification. To invoke this event, do one of the following:

-   Set or update a session or local storage value with [**setItem**](/apis/web-storage/Storage/setItem).
-   Remove a session or local storage value with [**removeItem**](/apis/web-storage/Storage/removeItem).

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages (MSDN)

-   `frameSet`
-   `window`
-   `Introduction to Web Storage`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

