---
title: valueMissing
attributions:
  - 'Microsoft Developer Network: [[valueMissing Property](http://msdn.microsoft.com/en-us/library/ie/hh773370(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [[Making forms fabulous](http://www.html5rocks.com/en/tutorials/forms/html5forms/) article]'
notes:
  - 'requires example... checked out for me to provide.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/ValidityState
    href: /dom/ValidityState
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/ValidityState
standardization_status: 'W3C Working Draft'
summary: 'Returns whether a value has not been entered in an input field that is required.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/ValidityState/valueMissing

---
## <span>Summary</span>

Returns whether a value has not been entered in an input field that is required.

Property of [dom/ValidityState](/dom/ValidityState)[dom/ValidityState](/dom/ValidityState)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.validity.valueMissing;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether a value has not been entered in an input field that is required.

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Living Standard

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
