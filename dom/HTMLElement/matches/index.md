---
title: 'matches'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/API/Element.matches)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility, general clean-up/review for accuracy'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
standardization_status: 'W3C Working Draft'
summary: 'Returns true if an element matches a given selector. Otherwise, false.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLElement/matches

---
## Summary

Returns true if an element matches a given selector. Otherwise, false.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.matches(selector);
```

## Parameters

### selector

 Data-type
:   String

 This string represents the selector to test the element against. This parameter is required and it must have a length of at least one. An empty string throws the error `Dom Exception 12.`

## Return Value

Returns an object of type DOM NodeDOM Node

Returns true if the element matches the given selector or false if it doesn't.

**Needs Examples**: This section should include examples.

## Usage

     Currently, few browsers support the unprefixed version. It is recommended to use the API as following:

    var docEl = document.documentElement,
        matches = docEl.matches || docEl.webkitMatchesSelector || docEl.mozMatchesSelector || docEl.msMatchesSelector || docEl.oMatchesSelector;
    matches.call(element, selector)
