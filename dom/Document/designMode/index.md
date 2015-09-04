---
title: designMode
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs compat table'
summary: 'Sets or gets a value that indicates whether the document can be edited.'
uri: dom/Document/designMode

---
# designMode

## Summary

Sets or gets a value that indicates whether the document can be edited.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var designMode = document.designMode;
document.designMode = newDesignMode;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

"on" if the the document is editable, or "off" if it is not. Default is "off".

## Examples

This example toggles the state of document.designMode when the window is double-clicked.

``` {.html}
<!DOCTYPE HTML>
<html>
<head>
<script>
window.ondblclick = toggleDesignMode;

function toggleDesignMode() {
  alert(document.designMode);
  document.designMode = (document.designMode == "on") ? "off" : "on";
  alert(document.designMode);
}
</script>
</head>

<body>
This is a paragraph, which may or may not be editable.
</body>
</html>
```

## Usage

     Use the designMode property to let the user edit the current document.

While the browser is in design mode, objects enter a UI-activated state when the user presses `ENTER`, clicks an object that has focus, or double-clicks the object. Objects that are UI-activated have their own window in the document. You can modify the UI only when the object is in a UI-activated state.

## Notes

-   You cannot execute script when the value of the **designMode** property is set to **on**.
-   The default value is **off**.

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/editing.html#designMode)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/editing.html#designMode)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

