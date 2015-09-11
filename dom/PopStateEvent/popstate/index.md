---
title: popstate
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[popstate](https://developer.mozilla.org/en-US/docs/Web/Events/popstate) Article]'
  - 'Microsoft Developer Network: [[popstate Event](http://msdn.microsoft.com/en-us/library/ie/hh771875(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'An event handler that is fired when changes are made to the active history. Calls to pushState or replaceState can trigger this event.'
tags:
  - Events
  - DOM
uri: dom/PopStateEvent/popstate

---
## <span>Summary</span>

An event handler that is fired when changes are made to the active history. Calls to pushState or replaceState can trigger this event.

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
None

</td>
</tr>
</table>
## <span>Examples</span>

``` js
window.onpopstate = function(event) {
  alert("location: " + document.location + ", state: " + JSON.stringify(event.state));
};
history.pushState({page: 1}, "title 1", "?page=1");
history.pushState({page: 2}, "title 2", "?page=2");
history.replaceState({page: 3}, "title 3", "?page=3");
history.back(); // alerts "location: http://example.com/example.html?page=1, state: {"page":1}"
history.back(); // alerts "location: http://example.com/example.html, state: null
history.go(2);  // alerts "location: http://example.com/example.html?page=3, state: {"page":3}
```

### <span>Syntax</span>

### <span>Event handler parameters</span>

*val* [in]
:   Type: **Function** A script function to do something when the event is fired.
