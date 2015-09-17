---
title: 'ms-wrap-through'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Browser bias. Needs summary, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/exclusions
    href: '/w/index.php?title=css/exclusions&action=edit&redlink=1'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/exclusions
uri: css/exclusions/ms-wrap-through

---
Property of [css/exclusions](/w/index.php?title=css/exclusions&action=edit&redlink=1)[css/exclusions](/w/index.php?title=css/exclusions&action=edit&redlink=1)

## Syntax

``` js
var result = element.ms-wrap-through;
element.ms-wrap-through = value;
```

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

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   Internet Explorer 10 Guide for Developers: CSS Exclusions[Internet Explorer 10 Guide for Developers: CSS Exclusions](http://go.microsoft.com/fwlink/p/?LinkId=236927)
