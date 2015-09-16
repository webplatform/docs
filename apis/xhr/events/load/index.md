---
title: load
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
summary: "After the onload event has occurred,\nresponseText contains the complete server response.\n"
tags:
  - Events
uri: apis/xhr/events/load

---
## Summary

After the onload event has occurred, responseText contains the complete server response.

## Overview Table

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
No

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
</td>
</tr>
</table>
## Examples

Setting the **onload** property.

``` js
function loadd()
{
    alert("XDR onload");
    alert("Got: " + xdr.responseText);
}
...
xdr.onload = loadd;
```

## Notes

### Remarks

After the **onload** event has occurred, **responseText** contains the complete server response. To invoke this event, do one of the following:

-   Event handlers are called as needed after a request is **sent**.

### Event handler parameters

This method has no parameters.

## See also

### Related pages

-   `XDomainRequest`
-   `Reference`
-   `onprogress`
-   `Conceptual`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`
