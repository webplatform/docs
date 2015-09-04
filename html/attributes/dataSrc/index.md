---
title: dataSrc
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'Sets or retrieves the source of the data for data binding.'
uri: html/attributes/dataSrc
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/getAttribute

---
# dataSrc

## Summary

Sets or retrieves the source of the data for data binding.

Applies to
:    ?

## Examples

In this example, a text box is bound to the customer\_name field of a data source object with an ID of "customer." Because the text box is located in a data-bound [**table**](/html/elements/table), it is repeated to display each of the records provided by the data source.

    <table datasrc="#customer">
       <tr><td><input type="textbox" datafld="customer_name"><td><tr>
    </table>

## Notes

### Remarks

The [**dataFld**](/html/attributes/dataFld) property is not available on **param** objects; use [**getAttribute('dataFld')**](/w/index.php?title=dom/methods/getAttribute&action=edit&redlink=1) instead. Tabular and single-valued data consumers use the **dataSrc** property to specify a binding. The property takes a string that corresponds to the unique identifier of a data source object (DSO) on the page. The string must be prefixed by a number sign (\#). When the **dataSrc** property is applied to a tabular data consumer, the entire data set is repeated by the consuming elements. When the **dataSrc** property is applied to a [**table**](/html/elements/table), any contained single-valued consumer objects that specify a [**dataFld**](/html/attributes/dataFld) property are repeated for each record in the supplied data set. To complete the binding, the binding agent interrogates the enclosing **table** for its data source. A tabular data consumer contained within another tabular data consumer (**table**) must specify an explicit **dataSrc**.

### Syntax

## See also

### Related pages (MSDN)

-   `a`
-   `applet`
-   `button`
-   `div`
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
-   `option`
-   `select`
-   `span`
-   `table`
-   `textArea`
-   `Introduction to Data Binding`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

