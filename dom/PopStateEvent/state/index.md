---
title: state
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
summary: 'The current history entry''s state object (if any).'
uri: dom/PopStateEvent/state
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/objects/PopStateEvent

---
# state

## Summary

The current history entry's state object (if any).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/PopStateEvent](/dom/PopStateEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.state;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

Represents the context information for the event, or null, if the state represented is the initial state of the document.

## Examples

``` {.js}
window.onpopstate = function(event) {
  alert("location: " + document.location + ", state: " + JSON.stringify(event.state));
};
```

## Notes

### Remarks

Represents the context information for the event, or **null**, if the state represented is the initial state of the document.

### Syntax

## See also

### Related pages (MSDN)

-   `PopStateEvent`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[state Property](http://msdn.microsoft.com/en-us/library/ie/hh772351(v=vs.85).aspx) Article]

