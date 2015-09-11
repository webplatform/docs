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
## <span>Summary</span>

After the onload event has occurred, responseText contains the complete server response.

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
## <span>Examples</span>

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

## <span>Notes</span>

### <span>Remarks</span>

After the **onload** event has occurred, **responseText** contains the complete server response. To invoke this event, do one of the following:

-   Event handlers are called as needed after a request is **sent**.

### <span>Event handler parameters</span>

This method has no parameters.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `XDomainRequest`
-   `Reference`
-   `onprogress`
-   `Conceptual`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`
