---
title: clearInterval
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Cancels the interval previously started using the setInterval method. '
uri: dom/Window/clearInterval

---
# clearInterval

## Summary

Cancels the interval previously started using the setInterval method.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
 window.clearInterval(/* see parameter list */);
```

## Parameters

### timerID

 Data-type�
:   Number

**Integer** that specifies the interval to cancel. This value must have been previously returned by the [**setInterval**](/dom/Window/setInterval) method.

## Return Value

No return value

## Examples

``` {.html}
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>setInterval/clearInterval example</title>
<script>
var nIntervId;

function changeColor() {
  nIntervId = setInterval(flashText, 500);
}

function flashText() {
  var oElem = document.getElementById("my_box");
  oElem.style.color = oElem.style.color == "red" ? "blue" : "red";
}

function stopTextColor() {
  clearInterval(nIntervId);
}
</script>
</head>

<body onload="changeColor();">
<div id="my_box" style="color: red;">
<p>Hello World</p>
</div>
<button onclick="stopTextColor();">Stop</button>

</body>
</html>
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[clearInterval](https://developer.mozilla.org/en-US/docs/Web/API/Window.clearInterval) Article]

Portions of this content come from the Microsoft Developer Network: [[clearInterval Method](http://msdn.microsoft.com/en-us/library/ie/ms536353(v=vs.85).aspx) Article]

