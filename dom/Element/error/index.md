---
title: 'error'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, compat, better spec link'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
tags:
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/file/MSStream
uri: dom/Element/error

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.error;
element.error = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Fires the **onerror** event and passes the associated error to the **error** property. Error codes map directly to World Wide Web Consortium (W3C) file errors, as described in the following table.

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">NotFoundError</td>
<td align="left">The resource (<a href="/apis/file/File"><strong>File</strong></a>, <a href="/apis/file/Blob"><strong>Blob</strong></a>, or <a href="/w/index.php?title=apis/file/MSStream&amp;action=edit&amp;redlink=1"><strong>msStream</strong></a>) could not be found at the time the read was processed.</td>
</tr>
<tr class="even">
<td align="left">SecurityError</td>
<td align="left">One of the following occurred:
<ul>
<li>The file being accessed is unsafe.</li>
<li>The file has changed since the user selected it.</li>
<li>Other security issues not covered by other error types.</li>
</ul></td>
</tr>
<tr class="odd">
<td align="left">NotReadableError</td>
<td align="left">The resource could not be read. This may occur due to permission problems on the file.</td>
</tr>
<tr class="even">
<td align="left">EncodingError</td>
<td align="left">The resource could not be encoded due to data URL length limitations.</td>
</tr>
</tbody>
</table>

  This property is `null` unless there is an error.

### Syntax

## See also

### Related pages

-   FileReader[FileReader](/apis/file/FileReader)
-   msStreamReader[msStreamReader](/apis/file/MSStreamReader)
