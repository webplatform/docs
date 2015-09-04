---
title: setTimeout
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
summary: 'Evaluates an expression after a specified number of milliseconds has elapsed. '
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setTimeout.htm'
uri: dom/Window/setTimeout

---
# setTimeout

## Summary

Evaluates an expression after a specified number of milliseconds has elapsed.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
var timeoutId = window.setTimeout(/* see parameter list */);
```

## Parameters

### expression

 Data-type�
:   String

**Variant** that specifies the function pointer or string that indicates the code to be executed when the specified interval has elapsed.

### msec

 Data-type�
:   String

**Integer** that specifies the number of milliseconds.

### language

 Data-type�
:   String

*(Optional)*

**String** that specifies one of the following values:

## Return Value

Returns an object of type Number.

**Integer**

Integer. Returns an identifier that cancels the evaluation with the [**clearTimeout**](/dom/Window/clearTimeout) method.

## Examples

The following example uses the **setTimeout** method to evaluate a simple expression after one second has elapsed.

``` {.js}
window.setTimeout("alert('Hello, world')", 1000);
```

The following example uses the **setTimeout** method to evaluate a slightly more complex expression after one second has elapsed.

``` {.js}
var sMsg = "Hello, world";
window.setTimeout("alert(" + sMsg + ")", 1000);
```

This example uses the **setTimeout** method to hide a **input type=button** object after three seconds. If the user clicks the **Count Down** button and then counts to three, the **Now You See Me** button disappears.

``` {.js}
<script type="text/javascript">
function fnHide(oToHide){
   window.setTimeout("fnHide2(" + oToHide.id + ")", 3000);
}
function fnHide2(sID){
   var o = eval(sID);
   o.style.display="none";
}
</script>
<input type="button" value="Count Down"
    id="oHideButton" onclick="fnHide(this)">
```

This example uses a function pointer to pass the data. In this case, the data is stored in a global variable because it cannot be passed directly. In the preceding example, the [**ID**](/html/attributes/id) of the button is passed as a parameter to the function invoked by the **setTimeout** method. This is possible only when a string is passed as the first argument.

``` {.js}
<script type="text/javascript">
var g_oToHide = null;
function fnHide(oToHide){
    g_oToHide = oToHide;
    window.setTimeout(fnHide2, 3000);
}
function fnHide2(sID){
    if (g_oToHide) {
       g_oToHide.style.display="none";
    }
}
</script>
<input type="button" value="Now you see me ..."
    id="oHideButton" onclick="fnHide(this)">
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setTimeout.htm)

## Notes

### Remarks

The specified expression or function is evaluated once. For repeated evaluation, use the [**setInterval**](/dom/Window/setInterval) method. When you use the **setTimeout** method with Introduction to DHTML Behaviors, the value of *expression* should be a function pointer to call a function within the HTML Component (HTC) file or a string to call a function in the primary document.

**Note**  In Windows Internet Explorer, you cannot pass arguments to the callback function directly; however, you can simulate passing arguments by creating an anonymous closure function that references variables within scope of the call to [**setInterval**](/dom/Window/setInterval) or **setTimeout**. In versions earlier than Microsoft Internet Explorer 5, the first argument of **setTimeout** must be a string. Evaluation of the string is deferred until the specified interval elapses. As of Internet Explorer 5, the first argument of **setTimeout** can be a string or a function pointer.

### Reliability & timeout clamping

This API does not guarantee that timers will run exactly on schedule. Delays due to CPU load, other tasks, etc, are to be expected. Additionally a setTimeout or [setInterval](/dom/Window/setInterval) call has a minimum interval of of 4 ms, as specified by the HTML4 spec.

Generally all browsers implement this timeout "clamp" to 4 ms, although some browsers also clamp to a higher value when the window is not focused. For instance, the minimum timeout for a setInterval call can be up to a second in Chrome when the tab is inactive.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[setTimeout](https://developer.mozilla.org/en-US/docs/Web/API/window.setTimeout) Article]

Portions of this content come from the Microsoft Developer Network: [[setTimeout Method](http://msdn.microsoft.com/en-us/library/ie/ms536753(v=vs.85).aspx) Article]

