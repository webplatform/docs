---
title: select
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/webcomponents/shadowdom/)'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'One or more tokens that define the matching criteria for the distribution of child nodes of the shadow host.'
tags:
  - Markup
  - Attributes
  - HTML
  - Shadow
  - DOM
uri: html/attributes/select

---
## Summary

One or more tokens that define the matching criteria for the distribution of child nodes of the shadow host.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
dom/HTMLContentElement

</td>
</tr>
</table>
The select tokens define the matching criteria for distributing child nodes of the shadow host. Each token must be a valid selector fragment, which consists of the following:

-   a selector that uniquely identifies the shadow host.
-   a combination selector that identifies the parent element and the element at this insertion point.
-   the following CSS3 [selectors](/css/selectors):
    -   [type selector](/css/selectors/type)
    -   [universal selector](/css/selectors/universal_selector)
    -   [class selector](/css/selectors/class_selector)
    -   [ID selector](/css/selectors/id_selector)
    -   [attribute selectors](/css/selectors/attribute_selector)
    -   The following pseudo-class selectors:
        -   link
        -   visited
        -   target
        -   enabled
        -   disabled
        -   checked
        -   indeterminate
        -   nth-child()
        -   nth-last-child()
        -   nth-of-type()
        -   nth-last-of-type()
        -   first-child
        -   last-child
        -   first-of-type
        -   last-of-type
        -   only-of-type

## Examples

This example uses CSS selectors to select specific content from a shadow root.

``` html
<div style="background: purple; padding: 1em;">
  <div style="color: red;">
    <content select=".first"></content>
  </div>
  <div style="color: yellow;">
    <content select="div"></content>
  </div>
  <div style="color: blue;">
    <content select=".email"></content>
  </div>
</div>
```

## Related specifications

[Shadow DOM](http://www.w3.org/TR/2012/WD-shadow-dom-20120522/)
:   W3C Working Draft
