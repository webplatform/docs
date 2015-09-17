---
title: 'NodeList'
notes:
  - 'Review for currentness, current DOM Working Draft says this is "old-style"'
standardization_status: 'W3C Recommendation'
summary: 'Represents a list of DOM Nodes'
tags:
  - API_Objects
  - DOM
uri: dom/NodeList

---
## Summary

Represents a list of DOM Nodes

## Properties

[length](/apis/NodeList/length)
:   The number of nodes in the list.

## Methods

[item](/dom/NodeList/item)
:   Gets the *n*th item in the collection

## Events

*No events.*

## Examples

``` js
var list = document.getElementsByClassName('highlighted');
for(var i=0; i<list.length; i++){
    var item = list[i];
}
```

## Notes

The NodeList represents the content as it is currently in the document, and will change as the document changes.

## Related specifications

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/level-one-core.html#ID-536297177)
:   W3C Recommendation

[DOM](http://www.w3.org/TR/dom/#nodelist)
:   W3C Working Draft
