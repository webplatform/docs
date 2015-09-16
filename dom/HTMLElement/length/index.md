---
title: length
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/length

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.length;
element.length = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **window**.**length** property returns the number of frames contained in a window. The **comment**.**length** property returns the number of characters in the object. Although this property is read-only for most objects, it is read/write for the [**areas**](/dom/HTMLMapElement/areas) collection (image maps), the [**options**](/dom/HTMLElement/options) collection (select boxes), and the **select** object. In all other cases, this property has read-only permission, which means you can retrieve, but cannot change, its current value. The **length** property does not count **input type=image** elements. To access all elements contained in a form use the [**children**](/dom/Element/children) property of the **HTMLElement**. This property is read-write on the areas collection for image maps and the options collection for select boxes. This allows a developer to shrink the collection. For Windows CE only, this collection will always be empty. As of Windows Internet Explorer 8, this property is read-only in the [**areas**](/dom/HTMLMapElement/areas) collection. In Microsoft Internet Explorer 6 and later, this property applies to the **comment** object.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
