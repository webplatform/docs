---
title: patternMismatch
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns whether the input field value does not match the rules defined by the pattern attribute.'
uri: dom/ValidityState/patternMismatch

---
# patternMismatch

## Summary

Returns whether the input field value does not match the rules defined by the pattern attribute.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/ValidityState](/dom/ValidityState)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.validity.patternMismatch;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether a value does not match the rules defined by the **pattern** attribute.

## Examples

The following example validates a UK Postal code field on the blur event handler. If an invalid UK postal code is entered, when the form is submitted the custom validity message is displayed.

``` {.js}
<script type="text/javascript">
function validatePostCode(evt){
var el=evt.target;
if(el.validity){
// HTML5 aware browsers
if(el.validity.patternMismatch){
el.setCustomValidity('Not a valid UK Postal Code.eg:G1 1AA ');
}else{
el.setCustomValidity("");
}
}else{
// fallback for legacy browsers.


}
}
document.getElementById('txtPostcode').addEventListener('blur',validatePostCode,false);
</script>
```

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## See also

### Other articles

[Regular Expression Library](http://www.regexlib.com/)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[patternMismatch Property](http://msdn.microsoft.com/en-us/library/ie/hh773355(v=vs.85).aspx) Article]

Portions of this content come from HTML5Rocks! [[Making forms fabulous](http://www.html5rocks.com/en/tutorials/forms/html5forms/) article]

