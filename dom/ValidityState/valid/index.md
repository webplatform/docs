---
title: valid
attributions:
  - 'Microsoft Developer Network: [[valid Property](http://msdn.microsoft.com/en-us/library/ie/hh773368(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [[Making forms fabulous](http://www.html5rocks.com/en/tutorials/forms/html5forms/) article]'
notes:
  - 'Needs example.... locked... will add example tomorrw'
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
summary: 'Returns whether the input field value has any validity errors.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/ValidityState/valid

---
## Summary

Returns whether the input field value has any validity errors.

Property of [dom/ValidityState](/dom/ValidityState)[dom/ValidityState](/dom/ValidityState)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.validity.valid;
```

## Return Value

Returns an object of type BooleanBoolean

Whether a value has no validity errors.

**Needs Examples**: This section should include examples.

## Notes

The following example displays all validation states for a validated field. **Note**  For code samples, see [Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128) and [Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131) on the Windows Internet Explorer sample site.

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
