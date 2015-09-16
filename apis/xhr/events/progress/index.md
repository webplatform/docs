---
title: 'progress'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
summary: "When the onprogress event occurs, \npartial data can be retrieved using responseText.\n"
tags:
  - Events
uri: apis/xhr/events/progress

---
## Summary

When the onprogress event occurs, partial data can be retrieved using responseText.

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

Setting the **onprogress** property.

``` js
function progres()
{
    alert("XDR onprogress");
    alert("Got: " + xdr.responseText);
}
...
xdr.onprogress = progres;
```

## Notes

### Remarks

When the **onprogress** event occurs, partial data can be retrieved using **responseText**. The onprogress event may occur 0, 1 or many times in the time interval between the [**onload**](/apis/xhr/events/load) event. To invoke this event, do one of the following:

-   Event handlers are called as needed after a request is **sent**.

### Event handler parameters

This method has no parameters.

## See also

### Related pages

-   `XDomainRequest`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`
