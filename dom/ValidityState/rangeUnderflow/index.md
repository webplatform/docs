---
title: 'rangeUnderflow'
attributions:
  - 'Microsoft Developer Network: [[rangeUnderflow Property](http://msdn.microsoft.com/en-us/library/ie/hh773360(v=vs.85).aspx) Article]'
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
summary: 'Returns whether a value is less than the min attribute on an input control.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/ValidityState/rangeUnderflow

---
## Summary

Returns whether a value is less than the min attribute on an input control.

Property of [dom/ValidityState](/dom/ValidityState)[dom/ValidityState](/dom/ValidityState)

## Syntax

**Note**: This property is read-only.

``` js
var rangeUnderflow = element.validity.rangeUnderflow;
```

## Return Value

Returns an object of type BooleanBoolean

Whether a value is less than the **min** attribute.

## Examples

The following example validates a numeric (type="number") input field on the onblur event handler. If a number outside the range values of the input control is entered the custom validity message is displayed when the form is submitted.

``` js
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

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
