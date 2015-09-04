---
title: clearTimeout
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Cancels a time-out that was set with the setTimeout method. '
uri: dom/Window/clearTimeout

---
# clearTimeout

## Summary

Cancels a time-out that was set with the setTimeout method.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
 window.clearTimeout(/* see parameter list */);
```

## Parameters

### timerID

 Data-typeÂ
:   Number

**Integer**Â that specifies the time-out setting returned by a previous call to the [**setTimeout**](/dom/Window/setTimeout) method.

## Return Value

No return value

## Examples

``` {.js}
var alarm = {
  remind: function(aMessage) {
    alert(aMessage);
    delete this.timeoutID;
  },

  setup: function() {
    this.cancel();
    var self = this;
    this.timeoutID = window.setTimeout(function(msg) {self.remind(msg);}, 1000, "Wake up!");
  },

  cancel: function() {
    if(typeof this.timeoutID == "number") {
      window.clearTimeout(this.timeoutID);
      delete this.timeoutID;
    }
  }
};
window.onclick = function() { alarm.setup() };
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[clearTimeout](https://developer.mozilla.org/en-US/docs/Web/API/Window.clearTimeout) Article]

Portions of this content come from the Microsoft Developer Network: [[clearTimeout Method](http://msdn.microsoft.com/en-us/library/ie/ms536357(v=vs.85).aspx) Article]

