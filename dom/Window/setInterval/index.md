---
title: 'setInterval'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[setInterval](https://developer.mozilla.org/en-US/docs/Web/API/Window.setInterval) Article]'
  - 'Microsoft Developer Network: [[setInterval Method](http://msdn.microsoft.com/en-us/library/ie/ms536749(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setInterval.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setInterval2.htm'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Window
summary: 'Evaluates an expression each time a specified number of milliseconds has elapsed.'
tags:
  - API_Object_Methods
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'tutorials/JavaScript gotchas/Why eval() is evil'
uri: dom/Window/setInterval

---
## Summary

Evaluates an expression each time a specified number of milliseconds has elapsed.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var object = object.setInterval(/* see parameter list */);
```

## Parameters

### expression

 Data-type
:   String

**Variant** that specifies a function pointer or string indicating the code to be executed when the specified interval has elapsed.

Passing a string as a parameter suffers the same hazards as [eval()](/w/index.php?title=tutorials/JavaScript_gotchas/Why_eval()_is_evil&action=edit&redlink=1), so it is generally recommended to pass a function pointer instead.

### msec

 Data-type
:   String

**Integer** that specifies the number of milliseconds.

Note that there may be a minimum interval for this function. See [setTimeout](/dom/Window/setTimeout).

### language

 Data-type
:   String

**String** that specifies any one of the possible values for the [**LANGUAGE**](/html/attributes/language) attribute.

## Return Value

Returns an object of type DOM NodeDOM Node

**Integer**

Integer. Returns an identifier that cancels the timer with the [**clearInterval**](/dom/Window/clearInterval) method.

## Examples

This example uses the **setInterval** method to create a DHTML clock. A variable is assigned to the interval, and can be used as a reference to stop the interval by using the [**clearInterval**](/dom/Window/clearInterval) method.

``` js
var oInterval = "";
function fnStartClock(){
   oInterval = setInterval(fnDoClock,200);
}
function fnDoClock(){
   // Code to display hours, minutes, and seconds.
}
window.onload = fnStartClock;
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setInterval.htm)

The next example demonstrates how to pass arguments to a function with [**setTimeout**](/dom/Window/setTimeout) or **setInterval**. To do this, create an inner anonymous function to wrap the real callback function. In the new function scope, you can refer to variables declared prior to the call to **setTimeout** (such as `div`). This structure is referred to as a "closure" in JScript

``` js
// The first example of a closure passes the variable to a named function.
function startTimer() {
    var div = document.getElementById('currentTime');
    setTimeout(function(){doClock(div)},200);
}
// The second example also uses a closure, by referring to an argument passed to the function.
function doClock(obj) {
    setInterval(function(){obj.innerHTML=(new Date()).toLocaleString()},200);
}
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setInterval2.htm)

This example demonstrates that more than one closure can refer to the same variable. Here, the callback function that displays the value of `count` is called at a different interval than the function that updates its value.

``` js
function startCounter() {
    var div = document.getElementById('counter');
    var count = 0;
    setInterval(function(){count++},143);
    setInterval(function(){div.innerHTML=count},667);
}
```

## Notes

### Remarks

The **setInterval** method continuously evaluates the specified expression until the timer is removed with the [**clearInterval**](/dom/Window/clearInterval) method. To pass a function as a string, be sure to append the function name with parentheses.

    window.setInterval("someFunction()", 5000);

When passing a function pointer, do not include the parentheses.

    window.setInterval(someFunction, 5000);

When you use the **setInterval** method with Introduction to DHTML Behaviors, the value of *expression* should be a function pointer to call a function within the HTML Component (HTC) file or a string to call a function in the primary document.

**Note**  In Windows Internet Explorer, you cannot pass arguments to the callback function directly; however, you can simulate passing arguments by creating an anonymous closure function that references variables within scope of the call to **setInterval** or [**setTimeout**](/dom/Window/setTimeout). For more information, see Examples. In versions earlier than Microsoft Internet Explorer 5, the first argument of **setInterval** must be a string. Evaluation of the string is deferred until the specified interval elapses. As of Internet Explorer 5, the first argument of **setInterval** can be passed as a string or as a function pointer.
