---
title: 'setImmediate'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[setImmediate](https://developer.mozilla.org/en-US/docs/Web/API/window.setImmediate) Article]'
  - 'Microsoft Developer Network: [[setImmediate Method](http://msdn.microsoft.com/en-us/library/ie/hh773176(v=vs.85).aspx) Article]'
code_samples:
  - 'http://ie.microsoft.com/testdrive/Performance/setImmediateSorting/Default.html'
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces.'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Window
standardization_status: Non-Standard
summary: 'Requests that a function be called when current or pending tasks are complete, such as events or screen updates.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Window/setImmediate

---
## Summary

Requests that a function be called when current or pending tasks are complete, such as events or screen updates.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var hTimer = window.setImmediate(/* see parameter list */);
```

## Parameters

### handler

 Data-type
:   any

 The function to be called.

### arguments

 Data-type
:   any

 Arguments to be passed to the function.

### retVal

 Data-type
:   any

 A handle to the request.

## Return Value

Returns an object of type NumberNumber

A handle to the request.S\_OK

**Integer**

A handle to the request.

## Examples

setImmediate Test Drive Demo

``` html

```

[View live example](http://ie.microsoft.com/testdrive/Performance/setImmediateSorting/Default.html)

## Notes

### Remarks

JavaScript operations run in the same thread as events, display updates, and other additional tasks. As a result, extended JavaScript operations (such as functions containing many lines of code) prevent additional tasks from being handled. In turn, this makes an application appear to be unresponsive because events (such as [**onclick**](/dom/MouseEvent/click) or [**onkeypress**](/dom/KeyboardEvent/keypress)) are not handled and the screen is not updated until the extended operation completes. The **setImmediate** method schedules the function specified in the **handler** parameter to run after the current script block completes. If additional actions are pending when the current script block completes, they are processed before the **handler** function is called. This effectively creates a *yield* between the current script block and the **handler** function. If you break extended operations into separate functions, you can use **setImmediate** to call each function in sequence. When you do this, **setImmediate** allows additional tasks to complete before calling each function in the sequence. In turn, this enables the application to respond to user input and to handle additional tasks in a predictable and responsive fashion.

**Note**   Some developers use [**setTimeout**](/dom/Window/setTimeout) (or [**setInterval**](/dom/Window/setInterval)) to create events that accomplish similar results; however, there are subtle, but important differences between the two techniques. The **setTimeout** method is restricted to 250 requests per second on most systems. This means that `setTimeout(0, handler)` waits roughly 4ms before executing, even if no additional actions are pending. In contrast, **setImmediate** yields between each request, no matter how many requests are waiting to processed. If no additional actions are pending, **setImmediate** calls the **handler** function immediately.
