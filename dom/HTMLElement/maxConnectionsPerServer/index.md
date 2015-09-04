---
title: maxConnectionsPerServer
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'summary, examples, general clean-up of MSDN import'
uri: dom/HTMLElement/maxConnectionsPerServer

---
# maxConnectionsPerServer

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.maxConnectionsPerServer;
element.maxConnectionsPerServer = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The maximum number of connections per server returned by the **maxConnectionsPerServer** property is determined by the HTTP version (1.0 or 1.1) used by the server. This number applies to any Web server connection, not just to downloads. The **maxConnectionsPerServer** attribute will return `6` on a broadband connection unless a user or an administrator has overridden the default settings. If the client computer is connected through dial-up, **maxConnectionsPerServer** will return `2` if connected to an HTTP 1.1 server or `4` if connected to an HTTP 1.0 server. To learn how to change the connection limits from their default values, see Connectivity Enhancements in Internet Explorer 8.

### Syntax

## See also

### Related pages (MSDN)

-   `window`
-   `Connectivity Enhancements in Internet Explorer 8`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

