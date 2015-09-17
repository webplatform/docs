---
title: 'isIndex'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: isIndex
  topic: html
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: '(Obsolete) A special-purpose single-line text input field'
tags:
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - HTML/Elements/a
    - HTML/Elements/input
    - dom/properties/tagName
uri: html/elements/isIndex

---
## Summary

(Obsolete) A special-purpose single-line text input field

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

This element was created to provide a single-line text-input control to allow any characters for entering a query string. The query string was supposed to be sent to the server identified by the base URL and return a list of pages matching this query.

## History

On June 1992, Dan Connolly would [prefer](http://1997.webhistory.org/www.lists/www-talk.1992/0080.html) a different [anchor](/w/index.php?title=HTML/Elements/a&action=edit&redlink=1) type instead of isindex.

On November 1992, [indexes as links rather than documents](http://lists.w3.org/Archives/Public/www-talk/1992NovDec/thread.html#31) started by Dan Connolly who is pushing the idea that indexes are more links than documents. In this thread, different type of solutions are proposed. The question of forms for making queries is [mentioned](http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0039.html) in reference to Dynatext browser: "The browser displays toggle buttons, text fields etc. The user fills in the fields, clicks OK, and the query results come up in the table of contents window."

A thread about [isindex](http://lists.w3.org/Archives/Public/www-talk/1992NovDec/thread.html#42) in November 1992, Kevin Hoadley [questioned](http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0042.html) the need for an isindex element and proposed to drop it. He proposed to have instead an [input](/w/index.php?title=HTML/Elements/input&action=edit&redlink=1) element (idea [supported](http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0053.html) by Steve Putz). Tim Berners-Lee [explains](http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0044.html) the purpose of isindex resulting in aggregated search results. Kevin [replies](http://lists.w3.org/Archives/Public/www-talk/1992NovDec/0048.html) that he doesn't like the boolean nature of isindex and would prefer a system where everything is searchable and proposes to extend the current WWW Framework with a specific httpd configuration and defined that some URIs mapping create search queries.

## Examples

This example uses the **ISINDEX** element to replace the default prompt.

``` html
<ISINDEX PROMPT="Enter a keyword to search for in the index">
```

## Notes

### Remarks

In HTML 4, this element is deprecated; **INPUT** is recommended for use instead. The [**tagName**](/w/index.php?title=dom/properties/tagName&action=edit&redlink=1) property for **isIndex** returns **input**. The **ISINDEX** element belongs in the **body** of the document. This element is treated as an **input** object inside a **form** object.
