---
title: initiatorType
tags:
  0: API
  1: Object
  2: Properties
  4: Resource
  5: Timing
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns a DOMString representing the type of object that initiated the request for the resource. See Return Value.'
uri: 'apis/resource timing/PerformanceResourceTiming/initiatorType'

---
# initiatorType

## Summary

Returns a DOMString representing the type of object that initiated the request for the resource. See Return Value.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/resource timing/PerformanceResourceTiming](/apis/resource_timing/PerformanceResourceTiming)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.initiatorType;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

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

This example assumes an HTML page containing a resource such as \<img src="[https://www.webplatform.org/logo/logo-with-text.png](https://www.webplatform.org/logo/logo-with-text.png)" /\>

``` {.js}
var resources = window.performance.getEntriesByType('resource');
alert("initiatorType: " + resources[0].initiatorType);
```

## Related specifications

Specification
:   Status
[W3C Resource Timing Specification](http://www.w3.org/TR/resource-timing/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

