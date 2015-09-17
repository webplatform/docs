---
title: 'stepMismatch'
attributions:
  - 'Microsoft Developer Network: [[stepMismatch Property](http://msdn.microsoft.com/en-us/library/ie/hh773362(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [[Making forms fabulous](http://www.html5rocks.com/en/tutorials/forms/html5forms/) article]'
readiness: 'Ready to Use'
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
summary: 'Returns whether the input field value does not fit the rules given by the step attribute.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/ValidityState/stepMismatch

---
## Summary

Returns whether the input field value does not fit the rules given by the step attribute.

Property of [dom/ValidityState](/dom/ValidityState)[dom/ValidityState](/dom/ValidityState)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.validity.stepMismatch;
```

## Return Value

Returns an object of type BooleanBoolean

Whether a value does not fit the rules given by the **step** attribute.

## Examples

The following example validates a numeric (type="number") input field on the onblur event handler. Since the step value is 2 and min and max are even, if a odd number is entered the custom validity message is displayed when the form is submitted.

``` js
<label>Enter a number between 4 and 20 that is a multiple of 2<br/>
<input id="myField" type="number" required  min="4" max="20" step="2" /></label>
<script type="text/javascript">
var el=document.getElementById('myField');
function validFactor(evt){
var el=evt.target;
if(el.validity){
// HTML5 aware browsers
if(el.validity.stepMismatch){
el.setCustomValidity('The entered number is not divisible by 2.');
}else{
el.setCustomValidity("");
}
}else{
// legacy validation

}
}
el.addEventListener('blur',validFactor,false);
</script>
```

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
