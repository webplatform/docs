---
title: popstate
tags:
  - Events
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'An event handler that is fired when changes are made to the active history. Calls to pushState or replaceState can trigger this event.'
uri: dom/PopStateEvent/popstate

---
# popstate

## Summary

An event handler that is fired when changes are made to the active history. Calls to pushState or replaceState can trigger this event.

## Overview Table

Synchronous
:   No
Bubbles
:   Yes
Target
:   dom/Element
Cancelable
:   No
Default action
:   None

## Examples

``` {.js}
window.onpopstate = function(event) {
  alert("location: " + document.location + ", state: " + JSON.stringify(event.state));
};
history.pushState({page: 1}, "title 1", "?page=1");
history.pushState({page: 2}, "title 2", "?page=2");
history.replaceState({page: 3}, "title 3", "?page=3");
history.back(); // alerts "location: http://example.com/example.html?page=1, state: {"page":1}"
history.back(); // alerts "location: http://example.com/example.html, state: null
history.go(2);  // alerts "location: http://example.com/example.html?page=3, state: {"page":3}
```

### Syntax

### Event handler parameters

*val* [in]
:   Type: **Function** A script function to do something when the event is fired.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[popstate](https://developer.mozilla.org/en-US/docs/Web/Events/popstate) Article]

Portions of this content come from the Microsoft Developer Network: [[popstate Event](http://msdn.microsoft.com/en-us/library/ie/hh771875(v=vs.85).aspx) Article]

