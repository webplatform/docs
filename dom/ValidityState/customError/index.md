---
title: customError
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The element''s custom validity message has been set to a non-empty string by calling the element''s setCustomValidity() method.'
uri: dom/ValidityState/customError

---
# customError

## Summary

The element's custom validity message has been set to a non-empty string by calling the element's setCustomValidity() method.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/ValidityState](/dom/ValidityState)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var hasErrorStatus = element.validity.customError;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the element has raised a custom error.

## Examples

``` {.js}
var elem = document.getElementById('email_addr_confirm');
elem.addEventListener('blur', verifyEmail);

function verifyEmail(evt) {
  var emlcfm= evt.srcElement;
  var eml=document.getElementById('email_addr');
  if (emlcfm.value != eml.value) {
    // the provided value doesn’t match the primary email address
    emlcfm.setCustomValidity('The two email addresses must match.');
// the emlcfm.validity.customError is true;
  } else {
    // input is valid -- reset the error state, has to be an empty string
    emlcfm.setCustomValidity('');
```

// the emlcfm.validity.customError is false;

     }

}

</pre>

## Usage

     HTML5 Web form validation

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[customError Property](http://msdn.microsoft.com/en-us/library/ie/hh773352(v=vs.85).aspx) Article]

Portions of this content come from HTML5Rocks! [[Making forms fabulous](http://www.html5rocks.com/en/tutorials/forms/html5forms/) article]

