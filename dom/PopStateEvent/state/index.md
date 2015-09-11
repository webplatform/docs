---
title: state
attributions:
  - 'Microsoft Developer Network: [[state Property](http://msdn.microsoft.com/en-us/library/ie/hh772351(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/PopStateEvent
    href: /dom/PopStateEvent
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /dom/PopStateEvent
summary: 'The current history entry''s state object (if any).'
tags:
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/PopStateEvent
uri: dom/PopStateEvent/state

---
## <span>Summary</span>

The current history entry's state object (if any).

Property of [dom/PopStateEvent](/dom/PopStateEvent)[dom/PopStateEvent](/dom/PopStateEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.state;
```

## <span>Return Value</span>

Returns an object of type<span></span>

Represents the context information for the event, or null, if the state represented is the initial state of the document.

## <span>Examples</span>

``` js
window.onpopstate = function(event) {
  alert("location: " + document.location + ", state: " + JSON.stringify(event.state));
};
```

## <span>Notes</span>

### <span>Remarks</span>

Represents the context information for the event, or **null**, if the state represented is the initial state of the document.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `PopStateEvent`
