---
title: 'rangeOverflow'
attributions:
  - 'Microsoft Developer Network: [[rangeOverflow Property](http://msdn.microsoft.com/en-us/library/ie/hh773357(v=vs.85).aspx) Article]'
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
summary: 'Returns whether a value is greater than the max attribute on an input control.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/ValidityState/rangeOverflow

---
## Summary

Returns whether a value is greater than the max attribute on an input control.

Property of [dom/ValidityState](/dom/ValidityState)[dom/ValidityState](/dom/ValidityState)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.validity.rangeOverflow;
```

## Return Value

Returns an object of type BooleanBoolean

Whether a value is greater than the **max** attribute on an input control.

## Examples

The following example validates a numeric (type="number") input field on the onblur event handler. If a number outside the range values of the input control is entered the custom validity message is displayed when the form is submitted.

![ValidityState rangeOverflow customError.png](/assets/public/c/c2/ValidityState_rangeOverflow_customError.png)

``` html


<form>
<div class="form-group">
  <label for="ex_nbr4to20">Enter a number between 4 and 20</label>
  <input id="ex_nbr4to20" name="ex[nbr4to20]" class="form-control" type="number" required  min="4" max="20" step="2" placeholder="e.g. 6">
</div>
<input type="submit" value="Try Submitting" />
</form>
<script>
  var fieldElement=document.getElementById('ex_nbr4to20');
  function onBlurHandler(event){
    var field = event.target;
    console.log(field.validity, field.validity.rangeOverflow);
    if(!!field.validity) {
      if(!!field.validity.rangeOverflow){
        // Try setting a range over 20
        field.setCustomValidity("The number is outside of an acceptable range");
      } else {
        field.setCustomValidity(""); // Has to be an empty string
      }
    } else {
      // Legacy validation
    }
    //console.log(field.validity);
  }
  fieldElement.addEventListener('blur', onBlurHandler, false);
</script>
```

</pre>

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

}

}
