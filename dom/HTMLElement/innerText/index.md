---
title: innerText
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerText.htm'
notes:
  - 'summary, compatibility, clean-up of MSDN section headers/rearrange content to use WPD sections'
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
uri: dom/HTMLElement/innerText

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.innerText;
element.innerText = value;
```

## <span>Examples</span>

This example uses the **innerText** property to replace an object's contents. The object surrounding the text is not replaced.

``` html
<P ID=oPara>Here's the text that will change.</P>
:
<BUTTON onclick="oPara.innerText='WOW! It changed!'">Change text</BUTTON>
<BUTTON onclick="oPara.innerText='And back again'">Reset</BUTTON>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerText.htm)

## <span>Notes</span>

### <span>Remarks</span>

The **innerText** property is valid for block elements only. By definition, elements that do not have both an opening and closing tag cannot have an **innerText** property. The **innerText** property is read-only on the **html**, [**table**](/html/elements/table), **tBody**, **tFoot**, **tHead**, and **tr** objects. When the **innerText** property is set, the given string completely replaces the existing content of the object. You can set this property only after the [**onload**](/dom/Element/load) event fires on the **window**. When dynamically creating a tag using [**TextRange**](/dom/TextRange), [**innerHTML**](/dom/HTMLElement/innerHTML), or [**outerHTML**](/dom/HTMLElement/outerHTML), use scripting to create new events to handle the newly formed tags. Microsoft Visual Basic Scripting Edition (VBScript) is not supported. You can change the value of the **title** element using the [**title**](/html/elements/title) property. To change the contents of the [**table**](/html/elements/table), **tFoot**, **tHead**, and **tr** elements, use the table object model. For example, use the [**rowIndex**](/dom/HTMLElement/rowIndex) property or the [**rows**](/dom/HTMLElement/rows) collection to retrieve a reference to a specific table row. You can add or delete rows using the [**insertRow**](/dom/HTMLTableElement/insertRow) and [**deleteRow**](/dom/HTMLTableElement/deleteRow) methods. To retrieve a reference to a specific cell, use the [**cellIndex**](/dom/HTMLElement/cellIndex) property or the [**cells**](/html/attributes/cells) collection. You can add or delete rows using the [**insertCell**](/dom/HTMLTableElement/insertCell) and [**deleteCell**](/dom/HTMLTableElement/deleteCell) methods. To change the content of a particular cell, use the [**innerHTML**](/dom/HTMLElement/innerHTML) property. **Security Warning:  ** The **innerText** property can be used to safely add dynamic text to a webpage if the target element type is not a `script` element. With the exception of the `script` element, **innerText** does not execute script when inserting text into the Document Object Model (DOM) of a webpage.

### <span>Syntax</span>