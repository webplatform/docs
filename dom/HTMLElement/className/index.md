---
title: 'className'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/className.htm'
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
uri: dom/HTMLElement/className

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.className;
element.className = value;
```

## Examples

This example uses the **className** attribute to apply one or more styles to an HTML element.

``` html
<HEAD>
    <STYLE TYPE="text/css">
        P {font-size: 24pt;}
        .redText {color: red;}
        .blueText {color: blue;}
        .italicText {font-style: italic;}
    </STYLE>
</HEAD>

<BODY>
    <P>
        Large text, no class specified, one implied.
    </P>
    <P CLASS="redText">
        Large text, .redText class specified.
    </P>
    <P CLASS="blueText italicText">
        Large text, .blueText and .italicText classes specified.
    </P>
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/className.htm)

## Notes

### Remarks

The class is typically used to associate a particular style rule in a style sheet with the element. You can apply multiple styles to an element by specifying more than one style for the **CLASS** attribute. To apply multiple styles to a single element, use the following syntax:

    <ELEMENT CLASS = "sClass [ sClass2 [ sClass3 ... ] ]" ... >

By default, the property is equal to the string assigned to the **className** property of the given object, or null if the attribute is not explicitly assigned. When multiple styles are specified for an element, a conflict could develop if two or more styles define the same attribute differently. In this case, you can resolve the conflict by applying styles to the element in the following order, according to the Cascading Style Sheets (CSS) selector used to define the style:

1.  Element
2.  **CLASS**
3.  [**ID**](/html/attributes/id)
4.  Inline styles

When two or more selectors pertain to an element, a style defined later takes precedence over a style defined earlier. For more information, see [Introduction to Cascading Style Sheets](http://msdn.microsoft.com/en-us/library/240ww6sz(VS.71).aspx). Multiple styles are supported as of Microsoft Internet Explorer 5. In Windows Internet Explorer 8, class names, such as `hslice` and `entry-title`, are used to identify portions of a webpage that can be monitored for updates (Web Slices). For more information, see Subscribing to Content with Web Slices.

### Syntax
