---
title: ms-wrap-through
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Browser bias. Needs summary, spec reference, standardization status'
uri: css/exclusions/ms-wrap-through
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/exclusions

---
# ms-wrap-through

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/exclusions](/w/index.php?title=css/exclusions&action=edit&redlink=1)</span></span>

## Syntax

``` {.js}
var result = element.ms-wrap-through;
element.ms-wrap-through = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

You can use the **-ms-wrap-through** property to control the effect of exclusions—for instance, to cause one content block to wrap around an exclusion element and another to intersect the same exclusion element. The *wrapping context* of a box is a collection of exclusion areas contributed by its associated exclusion boxes. When Windows Internet Explorer lays out a webpage, a box wraps its inline flow content in the area that corresponds to the subtraction of its wrapping context from its own content area. For more information about exclusion elements' impact on content flow, see the [Definitions](http://go.microsoft.com/fwlink/p/?LinkId=234931) section of the [CSS3 Exclusions](http://go.microsoft.com/fwlink/p/?LinkId=234148) specification.

### Syntax

`-ms-wrap-through: wrap | none`

### Standards information

-   [CSS Exclusions and Shapes Module Level 3](http://go.microsoft.com/fwlink/p/?linkId=234148), Section 3.3.1

## See also

### Related articles

#### Exclusions

-   [ms-wrap-flow](/css/exclusions/ms-wrap-flow)

-   **ms-wrap-through**

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `Internet Explorer 10 Guide for Developers: CSS Exclusions`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

