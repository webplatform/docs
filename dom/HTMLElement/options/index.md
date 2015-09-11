---
title: options
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
uri: dom/HTMLElement/options

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.options;
element.options = value;
```

## <span>Examples</span>

This example shows how to display the text and values of all **option** objects in the first **select** object in the document.

``` html
var coll = document.all.tags("SELECT");
if (coll.length>0) {
    for (i=0; i< coll(0).options.length; i++)
        alert("Element " + i + " is " + coll(0).options(i).text +
            " and has the value " + coll(0).options(i).value);
}
```

## <span>Notes</span>

### <span>Remarks</span>

To delete an **option** object from a **select** object, assign the **option** object a null value. This compresses the array. If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.