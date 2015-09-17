---
title: 'offsetParent'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/offsetParent

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.offsetParent;
element.offsetParent = value;
```

## Examples

This example shows how to determine the position of a **td** object. Although the **td** object appears to the far right in the document, its position is close to the x-axis and y-axis, because its offset parent is a [**table**](/html/elements/table) object rather than the document body.

``` html
<HTML>
<HEAD>
  <TITLE>Elements: Positions</TITLE>
  <SCRIPT LANGUAGE="JScript">

  function showPosition()
  {
    var oElement = document.all.oCell;

    alert("The TD element is at (" + oElement.offsetLeft +
          "," + oElement.offsetTop + ")\n" + "The offset parent is "
          + oElement.offsetParent.tagName );
  }
  </SCRIPT>
</HEAD>
<BODY onload="showPosition()">
<P>This document contains a right-aligned table.
<TABLE BORDER=1 ALIGN=right>
  <TR>
    <TD ID=oCell>This is a small table.</TD>
  </TR>
</TABLE>
</BODY>
</HTML>
```

[**Note**  For Internet Explorer 4.0, this same example returns a position of 0,0 because the offset parent is the table row. View live example]

## Notes

### Remarks

Most of the time the **offsetParent** property returns the **body** object. **Note**  In Microsoft Internet Explorer 5, the **offsetParent** property returns the [**table**](/html/elements/table) object for the **td** object; in Microsoft Internet Explorer 4.0 it returns the **tr** object. You can use the [**parentElement**](/dom/Element/parentElement) property to retrieve the immediate container of the table cell.

### Syntax
