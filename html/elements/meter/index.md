---
title: 'meter'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/meter)'
code_samples:
  - 'http://code.webplatform.org/gist/5281236'
  - 'http://code.webplatform.org/gist/5281393'
  - 'http://jsbin.com/ometoTE/4/edit'
compatibility:
  feature: meter
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLMeterElement](/w/index.php?title=dom/HTMLMeterElement&action=edit&redlink=1)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The HTML &lt;meter&gt; element represents a value within a specified range.  This value can be any real number.'
tags:
  - Markup_Elements
  - DOM
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLMeterElement
uri: html/elements/meter

---
## Summary

The HTML &lt;meter&gt; element represents a value within a specified range. This value can be any real number.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLMeterElement](/w/index.php?title=dom/HTMLMeterElement&action=edit&redlink=1)

<table class="wikitable">
<tr>
<th style="vertical-align: top" id="permitted-contents">
Permitted contents

</th>
<td style="vertical-align: top; padding-top: 10px">
Phrasing content, but may not contain any `<meter>` elements itself.

</td>
</tr>
<tr>
<th id="permitted-parents">
Permitted parents

</th>
<td>
Any element that can contain phrasing content.

</td>
</tr>
<tr>
<th id="tag-omission">
Tag omission

</th>
<td>
A `<meter>` element must have both a start tag and an end tag.

</td>
</tr>
</table>
 The meter element defines a value between a minimum or maximum. This can be used for fundraisers, test results, or a number of other things. It should not be used as a progress bar. For that, use the [progress element](/html/elements/progress). You should give a description of the meter within the tags, such as `<meter min="0" max="10" value="5">5 out of 10 squares occupied</meter>`. This meter can also have various attributes on it, such as the optimum, high and low values.

The content of the **meter** element should represent the set min/max/value attributes in human readable form. This will be picked up by assistive technologies as well as act as a fallback for browsers not supporting the element.

### Attributes

This element supports the HTML5 [global attributes](/html/global_attributes).

value
:   The current value of the meter. If there is no value specified, or if the value is incorrectly formatted, it defaults to 0. This value must be between the [min](#attribute-min) and [max](#attribute-max) values of the element. If not, it will default to the closest available value within the ranges.
optimum
:   The optimum, or goal value of the meter. For example, on a test score, this would be 100. Or, on a fundraiser, this may be a monetary value. This must be below the [max](#attribute-max) value and above the [min](#attribute-min) value.
min
:   The minimum value of the meter. This must be less than the [max](#attribute-max) attribute value. If this attribute is not present, it defaults to 0.
max
:   The maximum value of the meter. This must be greater than the [min](#attribute-min) attribute value. If this attribute is not present, it defaults to 1.
low
:   The low value is what is considered a low range for the meter. In the example of a fundraiser, it may be near the starting value. This must be greater than the [min](#attribute-min) and less than the [max](#attribute-max) and [high](#attribute-high) values. If unspecified, it defaults to 0.
high
:   The high value is what is considered a high range for the meter. In the example of a fundraiser, it may be near the goal value. This must be less than the [max](#attribute-max) and greater than the [min](#attribute-min) and [low](#attribute-low) values. If unspecified, it defaults to 1.

## Examples

A basic example of the meter element

``` html
<meter min="0" max="10" value="5">5 out of 10</meter>
```

[View live example](http://code.webplatform.org/gist/5281236)

An example of the meter element using all of its attributes

``` html
<meter min="0" max="1000" value="500" low="200" high="800" optimum="900">$500 raised</meter>
```

[View live example](http://code.webplatform.org/gist/5281393)

Styling options for the meter bar

``` css
meter {
  -webkit-appearance: none;
}

meter::-webkit-meter-bar {
  border: 2px solid black;
}

meter::-webkit-meter-bar {
  background: lightblue;
}

meter::-webkit-meter-optimum-value {
  background: green;
}

meter::-webkit-meter-suboptimum-value {
  background: orange;
}

meter::-webkit-meter-even-less-good-value {
  background: red;
}
```

[View live example](http://jsbin.com/ometoTE/4/edit)

## Usage

     The meter element is intended to have descriptive text inside of it, similar to the alt tag of the image element.

The title attribute may be used to specify a unit.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-meter-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-meter-element)
:   W3C Recommendation

## See also

### Other articles

-   [HTML5 progress element](/html/elements/progress)
