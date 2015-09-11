---
title: typeMismatch
attributions:
  - 'Microsoft Developer Network: [[typeMismatch Property](http://msdn.microsoft.com/en-us/library/ie/hh773366(v=vs.85).aspx) Article]'
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
summary: 'Returns whether the input field value is not the correct syntax.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/ValidityState/typeMismatch

---
## <span>Summary</span>

Returns whether the input field value is not the correct syntax.

Property of [dom/ValidityState](/dom/ValidityState)[dom/ValidityState](/dom/ValidityState)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.validity.typeMismatch;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether a value is not the correct syntax.

## <span>Examples</span>

In the following example validity.typeMismatch is used to validate an email address field instead of a regular expression pattern.

``` html
<!DOCTYPE html>
<html><head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<title>validity.typeMismatch</title>
</head>

<body>
<form name="frmRegister" id="frmRegister">
<label>Email Address:<br><input name="txtemail" id="txtemail" required="required" type="email"></label>
<input type="submit" value="Register..">
</form>
<script type="text/javascript">
function validEmail(evt){
var el=evt.target;
if(el.validity){
// html5 aware browsers
if(el.validity.typeMismatch){
el.setCustomValidity('Please enter a valid email address.');
}else{
el.setCustomValidity("");
}
}else{
// legacy validation

}
}
document.getElementById('txtemail').addEventListener('blur',validEmail,false);
</script>


</body></html>
```

## <span>Usage</span>

     Use to validate input fields of type email or url instead of patternMismatch.

## <span>Related specifications</span>

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
