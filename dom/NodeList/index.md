---
title: NodeList
notes:
  - 'Review for currentness, current DOM Working Draft says this is "old-style"'
standardization_status: 'W3C Recommendation'
summary: 'Represents a list of DOM Nodes'
tags:
  - API
  - Objects
  - DOM
uri: dom/NodeList

---
## <span>Summary</span>

Represents a list of DOM Nodes

## <span>Properties</span>

API Name
:   Summary

[length](/apis/NodeList/length)
:   The number of nodes in the list.

## <span>Methods</span>

API Name
:   Summary

[item](/dom/NodeList/item)
:   Gets the *n*th item in the collection

## <span>Events</span>

*No events.*

## <span>Examples</span>

``` js
var list = document.getElementsByClassName('highlighted');
for(var i=0; i<list.length; i++){
    var item = list[i];
}
```

## <span>Notes</span>

The NodeList represents the content as it is currently in the document, and will change as the document changes.

## <span>Related specifications</span>

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/level-one-core.html#ID-536297177)
:   W3C Recommendation

[DOM](http://www.w3.org/TR/dom/#nodelist)
:   W3C Working Draft
