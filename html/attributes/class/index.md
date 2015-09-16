---
title: class
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies one or more classes for an element, usually used to point to a class in a style sheet.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/class

---
## Summary

Specifies one or more classes for an element, usually used to point to a class in a style sheet.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
dom/HTMLElement

</td>
</tr>
</table>
## Examples

This example uses the class attribute to apply one or more styles to an HTML element.

``` html
<!doctype html>
<html>
  <head>
    <title></title>
    <style type="text/css">
        p {font-size: 24pt;}
        .redText {color: red;}
        .blueText {color: blue;}
        .italicText {font-style: italic;}
    </style>
  </head>
  <body>
    <p>
        Large text, no class specified, one implied.
    </p>
    <p class="redText">
        Large text, .redText class specified.
    </p>
    <p class="blueText italicText">
        Large text, .blueText and .italicText classes specified.
    </p>
  </body>
</html>
```

## Notes

### Remarks

The property is equal to NULL if the attribute is not explicitly assigned. When multiple styles are specified for an element, a conflict could develop if two or more styles define the same attribute differently. In this case, you can resolve the conflict by applying styles to the element in the following order, according to the Cascading Style Sheets (CSS) selector used to define the style:

1.  Element
2.  Class attribute
3.  ID attribute
4.  Inline styles

When two or more selectors pertain to an element, a style defined later takes precedence over a style defined earlier. For more information, see Introduction to Cascading Style Sheets.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## Related specifications

[HTML5](http://www.w3.org/TR/html5/)
:   W3C Recommendation
