---
title: moveToPoint
attributions:
  - 'Microsoft Developer Network: [[moveToPoint Method](http://msdn.microsoft.com/en-us/library/ie/ms536632(v=vs.85).aspx) Article]'
notes:
  - "Needs example with modern syntax... not for method.\nnot jScript. added new example,\n\nold example needs replacement."
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Moves the start and end positions of the text range to the given point.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/moveToPoint

---
## <span>Summary</span>

Moves the start and end positions of the text range to the given point.

Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## <span>Syntax</span>

``` js
var result = textRange.moveToPoint(/* see parameter list */);
```

## <span>Parameters</span>

### <span>x</span>

 Data-type
:   Number

**Integer** that specifies the horizontal offset relative to the upper-left corner of the window, in pixels.

### <span>y</span>

 Data-type
:   Number

**Integer** that specifies the vertical offset relative to the upper-left corner of the window, in pixels.

## <span>Return Value</span>

Returns an object of type NumberNumber

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

This example uses the **moveToPoint** method to move the text range to the point where the user clicked the mouse, expands the range, and selects the text within the new range.

``` html
<SCRIPT FOR=document EVENT=onclick LANGUAGE="JScript">
    var rng = document.body.createTextRange();
    rng.moveToPoint(window.event.x, window.event.y);
    rng.expand("word");
    rng.select();
</SCRIPT>
```

The following example moves the caret in harmony with the mouse as it moves over a contenteditable div element.

``` html
<!DOCTYPE html>
<html>
<head>
  <title>moveToPoint example</title>
</head>
<body>
  <div contenteditable="true" onmousemove="followMouse()">
    Move the mouse over this text, the caret will follow it.
  </div>
  <script type="text/javascript">
    function followMouse() {
      if (document.body.createTextRange) {
        var range = document.body.createTextRange();

        range.moveToPoint(event.clientX, event.clientY);
        range.select();
      }
    }
  &lt/script>
</body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

The coordinates of the point must be in pixels and be relative to the upper-left corner of the window. The resulting text range is empty, but you can expand and move the range using methods such as **expand** and [**moveEnd**](/dom/TextRange/moveEnd). This feature might not be available on non-Microsoft Win32 platforms.