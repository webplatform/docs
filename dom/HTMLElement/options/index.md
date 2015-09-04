---
title: options
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
standardization_status: Unknown
notes:
  - 'needs summary, clean-up of MSDN import'
uri: dom/HTMLElement/options

---
# options

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.options;
element.options = value;
```

## Examples

This example shows how to display the text and values of all **option** objects in the first **select** object in the document.

    var coll = document.all.tags("SELECT");
    if (coll.length>0) {
        for (i=0; i< coll(0).options.length; i++)
            alert("Element " + i + " is " + coll(0).options(i).text +
                " and has the value " + coll(0).options(i).value);
    }

## Notes

### Remarks

To delete an **option** object from a **select** object, assign the **option** object a null value. This compresses the array. If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

