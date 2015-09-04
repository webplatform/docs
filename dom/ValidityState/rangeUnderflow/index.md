---
title: rangeUnderflow
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns whether a value is less than the min attribute on an input control.'
uri: dom/ValidityState/rangeUnderflow

---
# rangeUnderflow

## Summary

Returns whether a value is less than the min attribute on an input control.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/ValidityState](/dom/ValidityState)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var rangeUnderflow = element.validity.rangeUnderflow;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether a value is less than the **min** attribute.

## Examples

The following example validates a numeric (type="number") input field on the onblur event handler. If a number outside the range values of the input control is entered the custom validity message is displayed when the form is submitted.

``` {.js}
<label>Enter a number between 4 and 20<br/>
<input id="myField" type="number" required  min="4" max="20" step="2" /></label>
<script type="text/javascript">
var el=document.getElementById('myField');
function validRange(evt){
var el=evt.target;
if(el.validity){
// HTML5 aware browsers
if(el.validity.rangeUnderflow){
el.setCustomValidity('The entered number is outside the acceptable range.');
}else{
el.setCustomValidity("");
}
}else{
// legacy validation

}
}
el.addEventListener('blur',validRange,false);
</script>
```

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[rangeUnderflow Property](http://msdn.microsoft.com/en-us/library/ie/hh773360(v=vs.85).aspx) Article]

Portions of this content come from HTML5Rocks! [[Making forms fabulous](http://www.html5rocks.com/en/tutorials/forms/html5forms/) article]

