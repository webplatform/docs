---
title: 'dataFormatAs'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: dataFormatAs
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Summary
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/getAttribute
uri: html/attributes/dataFormatAs

---
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
## Examples

The following **div** example renders data in HTML format.

``` html
<div datafld="Column2" dataformatas="html"></div>
```

The following **span** example renders data in HTML format.

``` html
<span datasrc="#bank_acct" datafld="balance" dataformatas="html"></span>
```

The following **textArea** example renders data in text format.

``` html
<textarea datasrc="#customer" datafld="address" dataformatas="text" rows=6 COLS=60></textarea>
```

## Notes

### Remarks

As of Windows Internet Explorer 7, the **DATAFORMATAS** attribute is no longer supported for the **input type=button** object. The [**dataFld**](/html/attributes/dataFld) property is not available on **param** objects; use [**getAttribute('dataFld')**](/w/index.php?title=dom/methods/getAttribute&action=edit&redlink=1) instead. Internet Explorer 5.01 or later honors the regional settings for the user's control panel when the **DATAFORMATAS** attribute is set to **localized-text**. Internet Explorer 5.01 or later performs a locale-dependent type conversion on the native value, instead of using the *data source object* to perform the conversion, when binding a textual element such as a **span**, **div**, or **input** to date, currency, or numeric data. Microsoft Internet Explorer 5 does not provide this feature. To compensate for this limitation, a *data source object* can implement **ISimpleDataConverter** to participate in the conversion. Neither of these features is supported in earlier versions of Windows Internet Explorer.

### Syntax

## See also

### Related pages

-   `button`
-   `div`
-   `input type=button`
-   `label`
-   `legend`
-   `marquee`
-   `object`
-   `option`
-   `select`
-   `span`
-   table[table](/html/elements/table)
-   `Introduction to Data Binding`
