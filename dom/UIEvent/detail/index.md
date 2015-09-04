---
title: detail
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
notes:
  - 'but.... example does not work in MSIE.'
summary: 'Gets additional, developer defined, information about an event.'
uri: dom/UIEvent/detail

---
# detail

## Summary

Gets additional, developer defined, information about an event.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/UIEvent](/dom/UIEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var eventDetails = event.detail;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

Returns additional numerical information about the event, depending on the type of event.

## Examples

``` {.html}
<!DOCTYPE html>
<html>
<head>
  <title>event.detail example</title>
  <script type="text/javascript">
  function giveDetails(e) {
      var text = document.getElementById("t");
      text.value = e.detail;
  }
  function init() {
      var b1 = document.getElementById("b");
      b1.onclick = giveDetails;
  }
  </script>
</head>
<body onload="init();">
<form>
 <input id="b" type="button" value="details"/>
 <input id="t" type="text" value=""/><br/>
 <input type="reset"/>
</form>
</body>
</html>
```

## Usage

     Use this property to get developer defined information about a developer generated event, if any. When part of a user agent initiated UIEvent, this property is never set.

## Notes

You can set the **detail** property of an event by using the [**initUIEvent**](/dom/UIEvent/initUIEvent) method.

For mouse events, such as click, dblclick, mousedown, or mouseup, the detail property indicates how many times the mouse has been clicked in the same location for this event.

For a dblclick event the value of detail is always 2.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.detail](https://developer.mozilla.org/en-US/docs/Web/API/event.detail) Article]

Portions of this content come from the Microsoft Developer Network: [[detail Property](http://msdn.microsoft.com/en-us/library/ie/ff974802(v=vs.85).aspx) Article]

