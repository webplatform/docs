---
title: ::after
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Inserts content after the selected element(s).'
tags:
  - CSS
  - Selectors
uri: 'css/selectors/pseudo-elements/::after'

---
## <span>Summary</span>

Inserts content after the selected element(s).

 The [**::before**](/css/selectors/pseudo-elements/::before) and **::after** pseudo-elements specify the location of content before and after an element in the document tree. The [**content**](/css/properties/content) attribute, in conjunction with these pseudo-elements, specifies what is inserted. The generated content interacts with other boxes as if they were real elements inserted just inside their associated element. The content box of the associated element expands to include the generated content, if necessary.

### <span>Syntax</span>

sel **::after**

### <span>Parameters</span>

*sel*
:   A simple selector

## <span>Examples</span>

``` css
span::after {
  content: " Required";
}
```

## <span>Notes</span>

Web authors are encouraged to use the two-colon form of the **::after** pseudo-element.

## <span>Related specifications</span>

[CSS 2.1](http://www.w3.org/TR/CSS2/)
:   W3C Recommendation

[Selectors Level 3](http://www.w3.org/TR/css3-selectors/)
:   W3C Recommendation

## <span>See also</span>

### <span>Related pages</span>

-   `content`
