---
title: returnValue
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Gets or sets a value that indicates whether to warn the user prior to navigating away from a page.'
uri: dom/BeforeUnloadEvent/returnValue

---
# returnValue

## Summary

Gets or sets a value that indicates whether to warn the user prior to navigating away from a page.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/BeforeUnloadEvent](/dom/BeforeUnloadEvent)</span></span>

## Syntax

``` {.js}
var returnValue = event.returnValue;
event.returnValue = preventNavigationReason;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The text that will be shown to the user.

## Examples

``` {.js}
//set returnValue to custom string
window.onbeforeunload = function (e) {
    e.returnValue = "About to navigate away from this page";
};
```

## Usage

     The BeforeUnloadEvent allows you to warn a user who is navigating away from a page or closing the browser. Set the return value to false or a string value to cancel the document unload event. You can also return a string or Boolean value from the event handler to display a message to the user, who is asked to confirm that they want to unload the document.

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

