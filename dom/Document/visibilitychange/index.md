---
title: visibilitychange
tags:
  - API
  - Object
  - Properties
  - DOM
  - Performance
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat tables'
summary: 'Set the visibility state of an element'
uri: dom/Document/visibilitychange

---
# visibilitychange

## Summary

Set the visibility state of an element

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var result = element.visibilitychange;
element.visibilitychange = value;
```

## Examples

``` {.js}
var timer = 0;
var PERIOD_VISIBLE = 1000;
var PERIOD_NOT_VISIBLE = 60000;

function onLoad() {
   timer = setInterval(checkEmail, (document.hidden) ? PERIOD_NOT_VISIBLE : PERIOD_VISIBLE);
   if(document.addEventListener) document.addEventListener("visibilitychange", visibilityChanged);
}

function visibilityChanged() {
   clearTimeout(timer);
   timer = setInterval(checkEmail, (document.hidden) ? PERIOD_NOT_VISIBLE : PERIOD_VISIBLE);
}

function checkEmail() {
   // Check server for new messages
}

window.onload = onLoad;
```

## Notes

### Remarks

This event is not triggered when it is registered.

### Syntax

### Event handler parameters

This method has no parameters.

## Related specifications

Specification
:   Status
[Page Visibility](http://www.w3.org/TR/page-visibility/)
:   Recommendation

## See also

### Related articles

#### Performance

-   [navigation timing](/apis/navigation_timing)

-   [resource timing](/apis/resource_timing)

-   [user timing](/apis/user_timing)

-   [hidden](/dom/Document/hidden)

-   [visibilityState](/dom/Document/visibilityState)

-   **visibilitychange**

-   [HTML5 Techniques for Optimizing Mobile Performance](/tutorials/mobile_opt_and_perf)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

