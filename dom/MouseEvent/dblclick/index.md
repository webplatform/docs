---
title: dblclick
tags:
  - Events
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'compatibility, more info'
summary: 'A mouse double click event.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ondblclickEX.htm'
uri: dom/MouseEvent/dblclick

---
# dblclick

## Summary

A mouse double click event.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:    ?

## Examples

This example uses the **dblclick** event to add items to a list box when the user double-clicks in the text box.

``` {.html}
<!doctype html>
<html>
 <head>
  <script>
function addItem() {
  sNewItem = new Option(txtEnter.value);
  selList.add(sNewItem);
}
  </script>
 </head>
 <body>
  <p>Enter text and then double-click in the text box to add text to the list box.
  <input type="text" name="txtEnter" value="Enter_text" ondblclick="addItem()">
  <select name="selList" size="5"></select>
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ondblclickEX.htm)

## Notes

The order of events leading to the **dblclick** event is [**mousedown**](/dom/MouseEvent/mousedown), [**mouseup**](/dom/MouseEvent/mouseup), [**click**](/dom/MouseEvent/click), **mouseup**, and then **dblclick**. Actions associated with any of these events are executed when the **dblclick** event fires. Initiates any action that is associated with the event. To invoke this event, do one of the following:

-   Click the left mouse button twice in rapid succession over an object. The user's double-click must occur within the time limit specified by the user's system.

## Related specifications

Specification
:   Status
[HTML 4.01](http://www.w3.org/TR/html401/)
:   Recommendation
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

