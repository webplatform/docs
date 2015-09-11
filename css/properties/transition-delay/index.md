---
title: transition-delay
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5841921'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0s`'
  'Applies to': "all elements,\_:before and\_:after pseudo elements"
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: interactive
  '[Computed value](/css/concepts/computed_value)': 'Same as specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`transitionDelay`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Defines when the transition will start. A value of ‘0s’ means the transition will execute as soon as the property is changed. Otherwise, the value specifies an offset from the moment the property is changed, and the transition will delay execution by that offset.'
tags:
  - CSS
  - Properties
uri: css/properties/transition-delay

---
## <span>Summary</span>

Defines when the transition will start. A value of ‘0s’ means the transition will execute as soon as the property is changed. Otherwise, the value specifies an offset from the moment the property is changed, and the transition will delay execution by that offset.

## <span>Overview table</span>

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
:   `transitionDelay`

Percentages
:   N/A

## <span>Syntax</span>

-   `transition-delay: time`

## <span>Values</span>

time
:   Floating-point number, followed by a time units designator (`ms` or `s`). For more information about the supported time units, see **CSS Values and Units Reference**.

Values are rounded up to the second decimal place. Each **transition-delay** is paired with a corresponding object property identified in the [**transition-property**](/css/properties/transition-property) property. If more **transition-delay** values are declared than corresponding object properties identified in the [**transition-property**](/css/properties/transition-property) property, the excess **transition-delay** values are ignored. If fewer **transition-delay** values are declared than corresponding object properties identified in the [**transition-property**](/css/properties/transition-property) property, the list of **transition-delay** values is repeated from the beginning until the object properties are exhausted.

## <span>Examples</span>

``` css
/*
 * This example shows a transition delay after hovering
 *  over a div for the specified delay time.
 *
 * In this example the background color will change
 * to red after hovering over a div for 3 seconds.
 */

div:hover{
    background-color: red;
    transition-delay: 3s;
}
```

[View live example](http://code.webplatform.org/gist/5841921)

### <span>Standards information</span>

-   [CSS Transitions Module Level 3](http://go.microsoft.com/fwlink/p/?linkid=223140), Section 2.4

## <span>Related specifications</span>

[CSS Transitions](http://www.w3.org/TR/2009/WD-css3-transitions-20091201/)
:   W3C Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Transitions</span>

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [transition](/css/properties/transition)

-   **transition-delay**

-   [transition-duration](/css/properties/transition-duration)

-   [transition-property](/css/properties/transition-property)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)
