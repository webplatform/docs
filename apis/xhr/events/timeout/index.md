---
title: timeout
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
summary: 'The ontimeout event occurs if the ontimeout period elapses before the onload event occurs.'
tags:
  - Events
uri: apis/xhr/events/timeout

---
## Summary

The ontimeout event occurs if the ontimeout period elapses before the onload event occurs.

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

Setting the **ontimeout** property.

``` js
<script type="text/javascript">
function timeo()
{
    alert("XDR ontimeout");
}
...
xdr.ontimeout = timeo;
```

## Notes

### Remarks

The **ontimeout** event occurs if the **ontimeout** period elapses before the [**onload**](/apis/xhr/events/load) event occurs. When the **ontimeout** event occurs, the **responseText** property is unavailable and attempts to access it will raise an error. To invoke this event, do one of the following:

-   Event handlers are called as needed after a request is **sent**.

### Event handler parameters

This method has no parameters.

## See also

### Related pages (MSDN)

-   `XDomainRequest`
-   `XMLHttpRequest`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`
