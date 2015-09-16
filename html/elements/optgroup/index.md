---
title: 'optgroup'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: optgroup
  topic: html
notes:
  - 'Add Category, Parent and Children information. Complete Compatibility table. Complete HTML information subsection.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLOptGroupElement](/dom/HTMLOptGroupElement)'
readiness: 'In Progress'
summary: 'Allows authors to group choices logically in a select element.'
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
uri: html/elements/optgroup

---
## Summary

Allows authors to group choices logically in a select element.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLOptGroupElement](/dom/HTMLOptGroupElement)

## Examples

The following example shows how to use the **OPTGROUP** element to create groups of items in a drop-down list box.

``` html
<SELECT>
    <OPTGROUP LABEL="Alkaline Metals">
        <OPTION>Lithium (Li)</OPTION>
        <OPTION>Sodium (Na)</OPTION>
        <OPTION>Potassium (K)</OPTION>
    </OPTGROUP>
    <OPTGROUP LABEL="Halogens">
        <OPTION>Fluorine (F)</OPTION>
        <OPTION>Chlorine (Cl)</OPTION>
        <OPTION>Bromine (Br)</OPTION>
    </OPTGROUP>
</SELECT>
```

## Notes

### Remarks

In [HTML 4.01](http://go.microsoft.com/fwlink/p/?linkid=203769), all **OPTGROUP** elements must be specified directly within a **SELECT** element. Groups may not be nested. You can add **OPTGROUP** elements only to a **SELECT** element located in the same window where the **OPTGROUP** elements are created. This element is available in HTML as of Microsoft Internet Explorer 6.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.6

### HTML information

{

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-optgroup-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-optgroup-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-OPTGROUP)
:   W3C Recommendation
