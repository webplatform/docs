---
title: designMode
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: 'W3C Working Draft'
summary: 'Sets or gets a value that indicates whether the document can be edited.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/designMode

---
## <span>Summary</span>

Sets or gets a value that indicates whether the document can be edited.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var designMode = document.designMode;
document.designMode = newDesignMode;
```

## <span>Return Value</span>

Returns an object of type StringString

"on" if the the document is editable, or "off" if it is not. Default is "off".

## <span>Examples</span>

This example toggles the state of document.designMode when the window is double-clicked.

``` html
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
<p>This is a paragraph, which may or may not be editable.</p>
</body>
</html>
```

## <span>Usage</span>

     Use the designMode property to let the user edit the current document.

While the browser is in design mode, objects enter a UI-activated state when the user presses `ENTER`, clicks an object that has focus, or double-clicks the object. Objects that are UI-activated have their own window in the document. You can modify the UI only when the object is in a UI-activated state.

## <span>Notes</span>

-   You cannot execute script when the value of the **designMode** property is set to **on**.
-   The default value is **off**.

## <span>Related specifications</span>

[W3C HTML5](http://www.w3.org/TR/html5/editing.html#designMode)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/editing.html#designMode)
:   Living Standard
