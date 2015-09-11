---
title: visibilitychange
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat tables'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Set the visibility state of an element'
tags:
  - API
  - Object
  - Properties
  - DOM
  - Performance
uri: dom/Document/visibilitychange

---
## <span>Summary</span>

Set the visibility state of an element

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var result = element.visibilitychange;
element.visibilitychange = value;
```

## <span>Examples</span>

``` js
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

## <span>Notes</span>

### <span>Remarks</span>

This event is not triggered when it is registered.

### <span>Syntax</span>

### <span>Event handler parameters</span>

This method has no parameters.

## <span>Related specifications</span>

[Page Visibility](http://www.w3.org/TR/page-visibility/)
:   Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Performance</span>

-   [navigation timing](/apis/navigation_timing)

-   [resource timing](/apis/resource_timing)

-   [user timing](/apis/user_timing)

-   [hidden](/dom/Document/hidden)

-   [visibilityState](/dom/Document/visibilityState)

-   **visibilitychange**

-   [HTML5 Techniques for Optimizing Mobile Performance](/tutorials/mobile_opt_and_perf)
