---
title: selectedIndex
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'needs summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
standardization_status: Unknown
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/selectedIndex

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.selectedIndex;
element.selectedIndex = value;
```

## <span>Examples</span>

This example uses the **selectedIndex** property to retrieve individual values from a **select** object. When a site is selected from the list, the browser displays the associated page.

``` html
<SELECT onchange="window.location.href=this.options
    [this.selectedIndex].value">
<OPTION VALUE="http://www.microsoft.com/ie">
    Internet Explorer</OPTION>
<OPTION VALUE="http://www.microsoft.com">
    Microsoft Home</OPTION>
<OPTION VALUE="http://msdn.microsoft.com">
    Developer Network</OPTION>
</SELECT>
```

## <span>Notes</span>

### <span>Remarks</span>

Options in a **select** object are indexed in the order in which they are defined, starting with an index of 0. When you set the **selectedIndex** property, the display of the **select** object updates immediately. The **selectedIndex** property returns -1 if a **select** object does not contain any selected items. Setting the selectedIndex property clears any existing selected items. The **selectedIndex** property is most useful when used with **select** objects that support selecting only one item at a time—that is, those in which the [**MULTIPLE**](/html/attributes/multiple) attribute is not specified. If the **MULTIPLE** attribute is specified for a **select** object, the **selectedIndex** property returns only the index of the first selected item, if any. The [**selected**](/html/attributes/selected) property is most useful when used with **select** objects that support selecting more than one item at a time—that is, those in which the [**MULTIPLE**](/html/attributes/multiple) attribute is specified. You can use the **selected** property to determine whether an individual item in a **select** object is selected. In addition, selected items are not cleared when the **selected** property is set. This allows multiple items in the list to be selected at the same time.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `select`
