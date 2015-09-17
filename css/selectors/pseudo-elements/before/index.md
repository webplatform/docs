---
title: '::before'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: '::before'
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: '::before creates a pseudo-element, which allows you to insert content onto a page from CSS before the selected element(s). The end result isn''t actually in the DOM, but it appears on the page as if it is. The pseudo-element is inline by default.'
tags:
  - CSS_Selectors
  - CSS
uri: 'css/selectors/pseudo-elements/::before'

---
## Summary

::before creates a pseudo-element, which allows you to insert content onto a page from CSS before the selected element(s). The end result isn't actually in the DOM, but it appears on the page as if it is. The pseudo-element is inline by default.

## Examples

``` css
p::before {
  content: 'Hello!';
}
```

## Notes

### Remarks

The **::before** and [**::after**](/css/selectors/pseudo-elements/::after) pseudo-elements specify the location of content before and after an element in the document tree. The [**content**](/css/properties/content) attribute, in conjunction with these pseudo-elements, specifies what is inserted. The generated content interacts with other boxes as if they were real elements inserted just inside their associated element. The content box of the associated element expands to include the generated content, if necessary. In Windows Internet Explorer 8, as well as later versions of Windows Internet Explorer in IE8 Standards mode, only the one-colon form of this pseudo-element is recognized—that is, **:before**. Beginning with Windows Internet Explorer 9, the **::before** pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form. Microsoft and the World Wide Web Consortium (W3C) encourage web authors to use the two-colon form of the **::before** pseudo-element. For more information, see the [Pseudo-elements](http://go.microsoft.com/fwlink/p/?LinkId=241611) section of the W3C's [CSS3 Selectors](http://go.microsoft.com/fwlink/p/?LinkId=241612) specification.

### Parameters

*sel*
:   A simple selector.

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 5.12.3

## Related specifications

[CSS Level 2 Specification](http://www.w3.org/TR/CSS2/)
:   W3C Recommendation

## See also

### Related pages

-   content[content](/css/properties/content)
