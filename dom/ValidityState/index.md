---
title: ValidityState
tags:
  - API
  - Objects
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Represents a validation state of an input element.'
uri: dom/ValidityState

---
# ValidityState

## Summary

Represents a validation state of an input element.

## Properties

API Name
:   Summary
[customError](/dom/ValidityState/customError)
:   The element's custom validity message has been set to a non-empty string by calling the element's setCustomValidity() method.
[patternMismatch](/dom/ValidityState/patternMismatch)
:   Returns whether the input field value does not match the rules defined by the pattern attribute.
[rangeOverflow](/dom/ValidityState/rangeOverflow)
:   Returns whether a value is greater than the **max** attribute on an input control.
[rangeUnderflow](/dom/ValidityState/rangeUnderflow)
:   Returns whether a value is less than the **min** attribute on an input control.
[stepMismatch](/dom/ValidityState/stepMismatch)
:   Returns whether the input field value does not fit the rules given by the **step** attribute.
[tooLong](/dom/ValidityState/tooLong)
:   Returns whether an input field's value is longer than is allowed by the **maxlength** attribute.
[typeMismatch](/dom/ValidityState/typeMismatch)
:   Returns whether the input field value is not the correct syntax.
[valid](/dom/ValidityState/valid)
:   Returns whether the input field value has any validity errors.
[valueMissing](/dom/ValidityState/valueMissing)
:   Returns whether a value has not been entered in an input field that is required.

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[ValidityState](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState) Article]

Portions of this content come from the Microsoft Developer Network: [[validityState Object](http://msdn.microsoft.com/en-us/library/ie/hh773263(v=vs.85).aspx) Article]

