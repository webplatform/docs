---
title: dataFld
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'Sets or retrieves a field of a given data source, as specified by the dataSrc property, to bind to the specified object.'
uri: html/attributes/dataFld
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/getAttribute

---
# dataFld

## Summary

Sets or retrieves a field of a given data source, as specified by the dataSrc property, to bind to the specified object.

Applies to
:    ?

## Examples

In this example, a text box is bound to the flavor field supplied by a data source object with an ID of `ice_cream`. Because the text box is contained in a table, it is repeated, and all values in the flavor column are displayed.

    <table datasrc="#ice_cream">
       <tr><td><input type="textbox" datafld="flavor"></td></tr>
    </table>

In this example, the **select** object is bound to the `card_type` column of a data source control with an ID of `order`. The value of the field in the data set determines the option that is initially selected. When the user selects a different option from the **select**, the value of the `card_type` field in the current record of the data set is updated.

    <select datasrc="#order" datafld="card_type">
       <option>Visa
       <option>Mastercard
       <option>American Express
       <option>Diner's Club
       <option>Discover
    </select>

## Notes

### Remarks

The **dataFld** property is not available on **param** objects; use [**getAttribute('dataFld')**](/w/index.php?title=dom/methods/getAttribute&action=edit&redlink=1) instead.

### Syntax

## See also

### Related pages (MSDN)

-   `a`
-   `applet`
-   `button`
-   `div`
-   `fieldSet`
-   `frame`
-   `iframe`
-   `img`
-   `input type=button`
-   `input type=checkbox`
-   `input type=hidden`
-   `input type=image`
-   `input type=password`
-   `input type=radio`
-   `input type=text`
-   `label`
-   `legend`
-   `marquee`
-   `object`
-   `param`
-   `select`
-   `span`
-   `textArea`
-   `Introduction to Data Binding`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

