---
title: outerText
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/outerText.htm'
notes:
  - 'summary, clean-up of MSDN import'
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
uri: dom/HTMLElement/outerText

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.outerText;
element.outerText = value;
```

## <span>Examples</span>

This example uses the **outerText** property to replace an object's content; the object itself also is replaced.

``` html
<DIV ID=oDiv>
<P ID=oPara>Here's the text that will change.</P>
</DIV>
:
<BUTTON onclick="oPara.outerText='WOW!
    It changed!'">Change text</BUTTON>
<BUTTON onclick="oDiv.innerHTML='<P ID=oPara>
    And back again</P>'">Reset</BUTTON>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/outerText.htm)

## <span>Notes</span>

### <span>Remarks</span>

The **outerText** property is read-only on the **html**, **tBody**, **td**, **tFoot**, **th**, **tHead**, and **tr** objects. When this property is set, the given string completely replaces the original text in the object. You can set this property only after the [**onload**](/dom/Element/load) event fires on the **window**. When dynamically creating a tag using [**TextRange**](/dom/TextRange), [**innerHTML**](/dom/HTMLElement/innerHTML), or [**outerHTML**](/dom/HTMLElement/outerHTML), use script to create new events to handle the newly formed tags. Microsoft Visual Basic Scripting Edition (VBScript) is not supported. You can change the value of the **title** element using the [**title**](/html/elements/title) property. To change the contents of the [**table**](/html/elements/table), **tFoot**, **tHead**, and **tr** elements, use the table object model. For example, use the [**rowIndex**](/dom/HTMLElement/rowIndex) property or the [**rows**](/dom/HTMLElement/rows) collection to retrieve a reference to a specific table row. You can add or delete rows using the [**insertRow**](/dom/HTMLTableElement/insertRow) and [**deleteRow**](/dom/HTMLTableElement/deleteRow) methods. To retrieve a reference to a specific cell, use the [**cellIndex**](/dom/HTMLElement/cellIndex) property or the [**cells**](/dom/HTMLTableElement/cellSpacing) collection. You can add or delete rows using the [**insertCell**](/dom/HTMLTableElement/insertCell) and [**deleteCell**](/dom/HTMLTableElement/deleteCell) methods. To change the content of a particular cell, use the [**innerHTML**](/dom/HTMLElement/innerHTML) property.

### <span>Syntax</span>