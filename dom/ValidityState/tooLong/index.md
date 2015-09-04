---
title: tooLong
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns whether an input field''s value is longer than is allowed by the maxlength attribute.'
uri: dom/ValidityState/tooLong

---
# tooLong

## Summary

Returns whether an input field's value is longer than is allowed by the maxlength attribute.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/ValidityState](/dom/ValidityState)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.validity.tooLong;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether a value is longer than is allowed by the **maxlength** attribute.

## Examples

In the following example the tooLong property is used to validate the length of text entered into a text area. However, the validity.tooLong is always false since text greater than the maxlength attribute value cannot be entered.

``` {.html}
<!DOCTYPE html>
<html><head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<title>validity.tooLong</title>
</head>

<body>
<form name="frmtwit" id="frmtwit">
<label>Message:<br><textarea id="txtMessage" maxlength="12"></textarea></label>
<input type="submit" value="Twit..">
</form>
<script type="text/javascript">
function validLength(evt){
var el=evt.target;
if(el.validity){
// html5 aware browsers
if(el.validity.tooLong){
el.setCustomValidity('Your twit is too long to be sent.');
}else{
el.setCustomValidity("");
}
}else{
// legacy validation

}
}
document.getElementById('txtMessage').addEventListener('blur',validLength,false);
</script>


</body></html>
```

## Usage

     There seems to be little usage for the tooLong validity state test as textarea and input elements do not allow text input past the maxlength value.

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[tooLong Property](http://msdn.microsoft.com/en-us/library/ie/hh773365(v=vs.85).aspx) Article]

Portions of this content come from HTML5Rocks! [[Making forms fabulous](http://www.html5rocks.com/en/tutorials/forms/html5forms/) article]

