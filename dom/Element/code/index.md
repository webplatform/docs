---
title: code
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, specs, compat'
readiness: 'Not Ready'
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
uri: dom/Element/code

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.code;
element.code = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The `code` property returns one of the following file error codes.

<table>
<col width="33%" />
<col width="33%" />
<col width="33%" />
<thead>
<tr class="header">
<th align="left">Constant</th>
<th align="left">Code</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">NotFoundError</td>
<td align="left">8</td>
<td align="left">The <a href="/apis/file/File"><strong>File</strong></a> or <a href="/apis/file/Blob"><strong>Blob</strong></a> could not be found at the time the read was processed.</td>
</tr>
<tr class="even">
<td align="left">SecurityError</td>
<td align="left">18</td>
<td align="left">A file error not covered by the other file error codes occurred, such as:
<ul>
<li>Too many read calls are being made on <a href="/apis/file/File"><strong>File</strong></a> or <a href="/apis/file/Blob"><strong>Blob</strong></a> resources.</li>
<li>The file has changed on disk since the user selected it.</li>
<li>Certain files are unsafe for access within a web application.</li>
</ul></td>
</tr>
<tr class="odd">
<td align="left">AbortError</td>
<td align="left">20</td>
<td align="left">The read operation was aborted, typically with a call to <a href="/apis/file/FileReader/abort"><strong>abort</strong></a>.</td>
</tr>
<tr class="even">
<td align="left">NotReadableError</td>
<td align="left">0</td>
<td align="left">The <a href="/apis/file/File"><strong>File</strong></a> or <a href="/apis/file/Blob"><strong>Blob</strong></a> cannot be read, typically due to permission problems that occur after a reference to a <strong>File</strong> or <strong>Blob</strong> has been acquired (that is, concurrent lock with another application).</td>
</tr>
<tr class="odd">
<td align="left">EncodingError</td>
<td align="left">0</td>
<td align="left">The length of the data URL for a <a href="/apis/file/File"><strong>File</strong></a> or <a href="/apis/file/Blob"><strong>Blob</strong></a> is too long.</td>
</tr>
</tbody>
</table>

  See [**FileError**](/apis/file/FileError) for a code example using these error codes.

### Syntax

## See also

### Related pages (MSDN)

-   `FileError`
-   `MSStreamError`
