---
title: 'ms-wrap-flow'
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
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/exclusions
uri: css/exclusions/ms-wrap-flow

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/exclusions](/w/index.php?title=css/exclusions&action=edit&redlink=1)[css/exclusions](/w/index.php?title=css/exclusions&action=edit&redlink=1)

## Syntax

``` js
var result = element.ms-wrap-flow;
element.ms-wrap-flow = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **-ms-wrap-flow** property makes an element an exclusion element when it has a computed value other than **auto**. This property specifies that the exclusion element (the exclusion) can be positioned in various ways, and that inline content will wrap around the exclusion in a way similar to how it wraps around floated elements. When the **-ms-wrap-flow** property's computed value is **auto**, the element does not become an exclusion element unless its [**float**](/css/properties/float) property's computed value is not **none**. In that case, the element contributes its border box to its containing block's wrapping context and content flows around it according to the [**clear**](/css/properties/clear) property. For more information about exclusion elements' impact on content flow, see the [Definitions](http://go.microsoft.com/fwlink/p/?LinkId=234931) section of the [CSS3 Exclusions](http://go.microsoft.com/fwlink/p/?LinkId=234148) specification.

### Syntax

`-ms-wrap-flow: auto | both | start | end | maximum | clear`

### Standards information

-   [CSS Exclusions and Shapes Module Level 3](http://go.microsoft.com/fwlink/p/?linkId=234148), Section 3.1.1

## See also

### Related articles

#### Exclusions

-   **ms-wrap-flow**

-   [ms-wrap-through](/css/exclusions/ms-wrap-through)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   Internet Explorer 10 Guide for Developers: CSS Exclusions[Internet Explorer 10 Guide for Developers: CSS Exclusions](http://go.microsoft.com/fwlink/p/?LinkId=236927)
