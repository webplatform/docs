---
title: 'hidden'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'document.hidden returns true if the document is hidden or false if it is visible at all'
tags:
  - API_Object_Properties
  - DOM
  - Performance
uri: dom/Document/hidden

---
## Summary

document.hidden returns true if the document is hidden or false if it is visible at all

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var state = document.hidden;
```

## Return Value

Returns an object of type BooleanBoolean

`hidden` is a boolean value which is `true` if the page is not visible, even the smallest part, and this typically happens when the tab is in background or the browser is minimized. It's important to note that this rule has some exceptions for accessibility tools that act in full-screen mode.

## Examples

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

## Notes

### Remarks

The **Visibility** API provides Web applications with the means to programmatically determine the current visibility of a page and be notified of visibility changes. You can use this property to determine whether a page is visible or not. If it is not visible, you can throttle page activity and resource usage to create more power- and CPU-efficient applications. This is a property of the **document** object. You can also use the [**visibilityState**](/dom/Document/visibilityState) and [**visibilitychange**](/dom/Document/visibilityState) properties to learn more about the page visibility state.

## Related specifications

[Page Visibility](http://www.w3.org/TR/page-visibility/#dom-document-hidden)
:   Recommendation

## See also

### Related articles

#### Performance

-   [navigation timing](/apis/navigation_timing)

-   [resource timing](/apis/resource_timing)

-   [user timing](/apis/user_timing)

-   **hidden**

-   [visibilityState](/dom/Document/visibilityState)

-   [visibilitychange](/dom/Document/visibilitychange)

-   [HTML5 Techniques for Optimizing Mobile Performance](/tutorials/mobile_opt_and_perf)

### Related pages

-   `window`
