---
title: 'transition-property'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/5842100'
compatibility:
  feature: transition-property
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`all`'
  'Applies to': "all elements,\_:before and\_:after pseudo elements"
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Same as specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`transitionProperty`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The ''transition-property'' property specifies the name of the CSS property to which the transition is applied.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/transition-property

---
## Summary

The 'transition-property' property specifies the name of the CSS property to which the transition is applied.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `all`

Applies to
:   all elements, :before and :after pseudo elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Same as specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `transitionProperty`

Percentages
:   N/A

## Syntax

-   `transition-property: all`
-   `transition-property: none`
-   `transition-property: propertyname`

## Values

none
:   No transition effect is applied (all transition properties are ignored) when a new property value is specified.

all
:   All properties that support transitions have the transition effect applied when a new value for the property is specified. (Default)

propertyname
:   A list of properties, separated by commas, to which the transition effect is applied.

## Examples

``` css
/*
  * This example only applies "transition-" prefixed css
  *  properties to those listed in "transition-property" css
  *  property(height and width).
  *
  * This example changes a hovered div's height and
  * width to 100px over a duration of 3s, any other css
  *  properties are applied happen instantly.
  *
  */
div:hover{
    background-color: red;
    height: 100px;
    width: 100px;
    transition-property: height, width;
    transition-duration:3s;
}
```

[View live example](http://code.webplatform.org/gist/5842100)

## Notes

### Remarks

The version of this property using a vendor prefix, **-ms-transition-property**, has been deprecated. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly.

### Standards information

-   [CSS Transitions Module Level 3](http://www.w3.org/TR/css3-transitions/#transition-property-property), Section 2.1

## Related specifications

[CSS Transitions](http://www.w3.org/TR/2009/WD-css3-transitions-20091201/)
:   W3C Working Draft

## See also

### Related articles

#### Transitions

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [transition](/css/properties/transition)

-   [transition-delay](/css/properties/transition-delay)

-   [transition-duration](/css/properties/transition-duration)

-   **transition-property**

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
