---
title: performance
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Should be under Window interface. Needs summary, example, spec reference'
uri: apis/timing/properties/performance
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/timing/properties/timing
    - apis/timing/properties/navigation

---
# performance

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/timing/objects/PerformanceEntry](/apis/timing/objects/PerformanceEntry)</span></span>

## Syntax

``` {.js}
var result = element.performance;
element.performance = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **performance** property returns a hosting area for performance timing objects. To create the hosting object, use the **window.performance** command. The hosting object has three attributes, which create performance timing objects:

-   [**timing**](/w/index.php?title=apis/timing/properties/timing&action=edit&redlink=1)
-   [**navigation**](/w/index.php?title=apis/timing/properties/navigation&action=edit&redlink=1)
-   [**memory**](/apis/timing/properties/memory)

### Syntax

### Standards information

-   [Navigation Timing](http://go.microsoft.com/fwlink/p/?linkid=210425), Section 4.4

## See also

### Related pages (MSDN)

-   `Window`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

