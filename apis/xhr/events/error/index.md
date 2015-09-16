---
title: 'error'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
summary: 'The onerror event occurs when the request could not be completed because of an error.'
tags:
  - Events
  - API
uri: apis/xhr/events/error

---
## Summary

The onerror event occurs when the request could not be completed because of an error.

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

Setting the onerror property.

``` js
<script type="text/javascript">
function err()
{
    alert("XDR onerror");
}
...
xdr.onerror = err;
```

## Notes

### Remarks

The document can respond to the error, but there is no way to determine the cause or nature of the error. The **onerror** event does not occur when the [**ontimeout**](/apis/xhr/events/timeout) event occurs. To invoke this event, do one of the following:

-   Cannot invoke.

### Event handler parameters

This method has no parameters.

## See also

### Related pages

-   `XDomainRequest`
-   `Reference`
-   onload[onload](/apis/xhr/events/load)
-   onprogress[onprogress](/apis/xhr/events/progress)
-   `Conceptual`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`
