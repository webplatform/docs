---
title: 'region-fragment'
compatibility:
  feature: region-fragment
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'CSS Regions'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`regionFragment`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: "Controls whether the last region in a chain displays additional 'overset' content according its default overflow property, or\tif it displays a fragment of content as if it were flowing into a subsequent region."
tags:
  - CSS_Properties
  - CSS
uri: css/properties/region-fragment

---
## Summary

Controls whether the last region in a chain displays additional 'overset' content according its default overflow property, or if it displays a fragment of content as if it were flowing into a subsequent region.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   CSS Regions

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `regionFragment`

Percentages
:   N/A

## Syntax

-   `region-fragment: auto`
-   `region-fragment: break`

## Values

auto
:   Region element displays [overset](/css/concepts/overset) content according to its [**overflow**](/css/properties/overflow) property.

break
:   Region element overrides [**overflow**](/css/properties/overflow) property, displaying whatever fragment of [overset](/css/concepts/overset) content can fit within the region.

## Examples

``` css
<style>
  article {
    flow-into: article-flow;
  }
  #region-1, #region-2 {
    flow-from: article-flow;
    region-fragment: break; /* or auto */
    overflow: visible; /* or hidden */
  }
</style>

<body>
  <article>...</article>
  <div id="region-1"></div>
  <div id="region-2"></div>
</body>
```

## Usage

     In the following example, 'region_1' can accommodate the article's gray text, 'region_2' can  accommodate the blue text, and the red  'overset' text does not fit within the region chain:

![region fragment.png](/assets/public/4/44/region_fragment.png)

Setting **region-fragment** to **break** suppresses display of the [overset](/css/concepts/overset) text, as shown in the example at the bottom. Setting **region-fragment** to its default **auto** value makes overset content display according to whatever [**overflow**](/css/properties/overflow) property is defined, as shown in the two examples on the right. Even **overflow:hidden** may display part of the first line of overset text.

The property only applies to the final element in a [*region chain*](/css/concepts/region_chain) that is not large enough to accomodate remaining content. To behave as a 'region', the element's [**flow-from**](/css/properties/flow-from) must specify a [named flow](/css/concepts/named_flow), and display content from a corresponding [**flow-into**](/css/properties/flow-into).

For an overview of CSS Regions, see [Using CSS Regions to flow content through a layout](/tutorials/css-regions).

## Notes

This property was formerly named **region-overflow**.

## Related specifications

[CSS Regions Module Level 1](http://www.w3.org/TR/css3-regions/)
:   W3C Working Draft

## See also

### External resources

-   W3C editor's draft: [CSS Regions Module Level 3](http://dev.w3.org/csswg/css3-regions/)
-   Adobe Web Standards: [CSS Regions](http://html.adobe.com/webstandards/cssregions)
-   Adobe Developer's Network: [CSS3 Regions: Rich page layout with HTML and CSS3](http://www.adobe.com/devnet/html5/articles/css3-regions.html)
-   [Sample pages](http://adobe.github.com/web-platform/samples/css-regions)
