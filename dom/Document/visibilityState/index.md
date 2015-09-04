---
title: visibilityState
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
summary: 'Returns the visibility state of a webpage.'
uri: dom/Document/visibilityState

---
# visibilityState

## Summary

Returns the visibility state of a webpage.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var visibilityState = document.visibilityState;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The current visibility state of the document, one of "hidden", "visible", "prerender", "unloaded".

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

Use the [**visibilitychange**](/dom/Document/visibilitychange) property to track changes to the visibility state.

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

-   **visibilityState**

-   [visibilitychange](/dom/Document/visibilitychange)

-   [HTML5 Techniques for Optimizing Mobile Performance](/tutorials/mobile_opt_and_perf)

### Related pages (MSDN)

-   `hidden`
-   `visibilitychange`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

