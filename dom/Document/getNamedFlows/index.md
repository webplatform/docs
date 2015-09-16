---
title: 'getNamedFlows'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Working Draft'
summary: 'Gathers NamedFlow objects, each representing a set of content that flows through various layout regions.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/getNamedFlows

---
## Summary

Gathers NamedFlow objects, each representing a set of content that flows through various layout regions.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var flows = document.getNamedFlows();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Returns a static [**NamedFlowCollection**](/apis/css-regions/NamedFlowCollection) object accessible via standard array methods. Each member is a [**NamedFlow**](/apis/css-regions/NamedFlow) instance representing a set of content that flows through various layout [regions](/css/concepts/region).

## Examples

Various ways to access [named flows](/css/concepts/named_flow):

``` js
var flow, flows;
flow = document.getNamedFlows().namedItem("main"); // typically by name
flow = document.getNamedFlows().item(0);
flow = document.getNamedFlows()[0];

flows = document.getNamedFlows();
for (var i = 0; i < flows.length; i++) {
    flow = flows[i];
    // do something with flow
}
```

## Related specifications

[CSS Regions Module Level 1](http://www.w3.org/TR/2013/WD-css3-regions-20130528/#document-getnamedflows)
:   Working Draft

## See also

### External resources

-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
