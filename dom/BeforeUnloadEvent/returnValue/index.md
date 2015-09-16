---
title: 'returnValue'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/BeforeUnloadEvent
    href: /dom/BeforeUnloadEvent
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/BeforeUnloadEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets or sets a value that indicates whether to warn the user prior to navigating away from a page.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/BeforeUnloadEvent/returnValue

---
## Summary

Gets or sets a value that indicates whether to warn the user prior to navigating away from a page.

Property of [dom/BeforeUnloadEvent](/dom/BeforeUnloadEvent)[dom/BeforeUnloadEvent](/dom/BeforeUnloadEvent)

## Syntax

``` js
var returnValue = event.returnValue;
event.returnValue = preventNavigationReason;
```

## Return Value

Returns an object of type StringString

The text that will be shown to the user.

## Examples

``` js
//set returnValue to custom string
window.onbeforeunload = function (e) {
    e.returnValue = "About to navigate away from this page";
};
```

## Usage

     The BeforeUnloadEvent allows you to warn a user who is navigating away from a page or closing the browser. Set the return value to false or a string value to cancel the document unload event. You can also return a string or Boolean value from the event handler to display a message to the user, who is asked to confirm that they want to unload the document.

## Related specifications

[HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
