---
title: performance
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Should be under Window interface. Needs summary, example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/timing/objects/PerformanceEntry
    href: /apis/timing/objects/PerformanceEntry
tags:
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/timing/properties/timing
    - apis/timing/properties/navigation
uri: apis/timing/properties/performance

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [apis/timing/objects/PerformanceEntry](/apis/timing/objects/PerformanceEntry)[apis/timing/objects/PerformanceEntry](/apis/timing/objects/PerformanceEntry)

## <span>Syntax</span>

``` js
var result = element.performance;
element.performance = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

The **performance** property returns a hosting area for performance timing objects. To create the hosting object, use the **window.performance** command. The hosting object has three attributes, which create performance timing objects:

-   [**timing**](/w/index.php?title=apis/timing/properties/timing&action=edit&redlink=1)
-   [**navigation**](/w/index.php?title=apis/timing/properties/navigation&action=edit&redlink=1)
-   [**memory**](/apis/timing/properties/memory)

### <span>Syntax</span>

### <span>Standards information</span>

-   [Navigation Timing](http://go.microsoft.com/fwlink/p/?linkid=210425), Section 4.4

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Window`
