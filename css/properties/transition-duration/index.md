---
title: transition-duration
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5842067'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0s`'
  'Applies to': "all elements,\_:before and\_:after pseudo elements"
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: interactive
  '[Computed value](/css/concepts/computed_value)': 'Same as specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`transitionDuration`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The ''transition-duration'' property specifies the length of time a transition animation takes to complete.'
tags:
  - CSS
  - Properties
uri: css/properties/transition-duration

---
## Summary

The 'transition-duration' property specifies the length of time a transition animation takes to complete.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0s`

Applies to
:   all elements, :before and :after pseudo elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   interactive

[Computed value](/css/concepts/computed_value)
:   Same as specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `transitionDuration`

Percentages
:   N/A

## Syntax

-   `transition-duration: time`

## Values

time
:   Floating-point number, followed by a time units designator (`ms` or `s`). For more information about the supported time units, see **CSS Values and Units Reference**.

## Examples

``` css
/*
  * This example gradually changes the background color
  * of a div to red over the specified duration time(3s)
  */
div:hover{
    background-color: red;
    transition-duration:3s;
}
```

[View live example](http://code.webplatform.org/gist/5842067)

## Notes

Transitions respect Cascading Style Sheets (CSS) box model constraints such as [**min-width**](/css/properties/min-width). For example, if an element is declared with a [**min-width**](/css/properties/min-width) value of `50px` then a transition to a width of `25px` is not valid. In a case such as this, the transition runs for the specified duration from the start value until a valid maximum or minimum end value, as appropriate.

### Standards information

-   [CSS Transitions Module Level 3](http://www.w3.org/TR/css3-transitions/#transition-duration-property), Section 2.2

## Related specifications

[CSS Transitions](http://www.w3.org/TR/2009/WD-css3-transitions-20091201/)
:   W3C Working Draft

## See also

### Related articles

#### Transitions

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [transition](/css/properties/transition)

-   [transition-delay](/css/properties/transition-delay)

-   **transition-duration**

-   [transition-property](/css/properties/transition-property)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
