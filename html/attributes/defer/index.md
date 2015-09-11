---
title: defer
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves the status of the script.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/defer

---
## <span>Summary</span>

Sets or retrieves the status of the script.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

Using the attribute at design time can improve the download performance of a document because the client does not need to parse and execute the script and can continue downloading and parsing the document instead.

### <span>Issues</span>

IE\<10 may interleave execution of scripts. [Discussion on Github.](https://github.com/h5bp/lazyweb-requests/issues/42)

Combining scrips both standard and with `defer` that depend on each other. [Discussion on Github.](https://github.com/zenorocha/browser-diet/issues/95#issuecomment-14852531)

## <span>See also</span>

### <span>Other articles</span>

<http://caniuse.com/#feat=script-defer>

### <span>Related pages (MSDN)</span>

-   `script`
