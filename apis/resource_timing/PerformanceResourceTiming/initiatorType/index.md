---
title: 'initiatorType'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: 'apis/resource timing/PerformanceResourceTiming'
    href: /apis/resource_timing/PerformanceResourceTiming
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/resource_timing/PerformanceResourceTiming
standardization_status: 'W3C Working Draft'
summary: 'Returns a DOMString representing the type of object that initiated the request for the resource. See Return Value.'
tags:
  - API_Object_Properties
  - API
  - Resource_Timing
uri: 'apis/resource timing/PerformanceResourceTiming/initiatorType'

---
## Summary

Returns a DOMString representing the type of object that initiated the request for the resource. See Return Value.

Property of [apis/resource timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)[apis/resource timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.initiatorType;
```

## Return Value

Returns an object of type

DOMString (one of the following):

-   css: The initiator is any CSS resource downloaded via the url() syntax, such as @import url(), background: url(), etc.
-   embed: The initiator is the src attribute of the HTML \<embed\> element.
-   img: The initiator is the src attribute of the HTML \<img\> element.
-   link: The initiator is the href attribute of the HTML \<link\> element.
-   object: The initiator is the data attribute of the HTML \<object\> element.
-   script: The initiator is the src attribute of the HTML \<script\> element.
-   subdocument: The initiator is the src attribute of the HTML \<frame\> or HTML \<iframe\> elements.
-   svg: The initiator is the \<svg\> element and all resources downloaded as children of the \<svg\> element.
-   xmlhttprequest: The initiator is a XMLHttpRequest object.
-   other: The initiator is not of any type listed above.

## Examples

This example assumes an HTML page containing a resource such as \<img src="<https://www.webplatform.org/logo/logo-with-text.png>" /\>

``` js
var resources = window.performance.getEntriesByType('resource');
alert("initiatorType: " + resources[0].initiatorType);
```

## Related specifications

[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft
