---
title: visibilityState
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
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Returns the visibility state of a webpage.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - Performance
uri: dom/Document/visibilityState

---
## <span>Summary</span>

Returns the visibility state of a webpage.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var visibilityState = document.visibilityState;
```

## <span>Return Value</span>

Returns an object of type StringString

The current visibility state of the document, one of "hidden", "visible", "prerender", "unloaded".

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

Use the [**visibilitychange**](/dom/Document/visibilitychange) property to track changes to the visibility state.

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

-   **visibilityState**

-   [visibilitychange](/dom/Document/visibilitychange)

-   [HTML5 Techniques for Optimizing Mobile Performance](/tutorials/mobile_opt_and_perf)

### <span>Related pages (MSDN)</span>

-   `hidden`
-   `visibilitychange`
