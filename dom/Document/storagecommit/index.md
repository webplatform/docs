---
title: 'storagecommit'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec, compat'
readiness: 'Not Ready'
tags:
  - Events
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/Document/storagecommit

---
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
 ?

</td>
</tr>
</table>
## Notes

### Remarks

Local storage is saved to disk asynchronously to improve performance. The **onstoragecommit** event can be used to determine when the disk storage has been updated. To invoke this event, do one of the following:

-   Set or update a local storage value with [**setItem**](/apis/web-storage/Storage/setItem).
-   Remove a local storage value with [**removeItem**](/apis/web-storage/Storage/removeItem).

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   `Introduction to Web Storage`
