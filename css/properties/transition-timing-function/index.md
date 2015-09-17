---
title: 'transition-timing-function'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://letmespellitoutforyou.com/samples/transit_delay.html'
  - 'http://letmespellitoutforyou.com/samples/transit_timing.html'
compatibility:
  feature: transition-timing-function
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`ease`'
  'Applies to': 'all elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: interactive
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`transitionTimingFunction`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Sets the pace of action within a transition'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/transition-timing-function

---
## Summary

Sets the pace of action within a transition

## Overview table

[Initial value](/css/concepts/initial_value)
:   `ease`

Applies to
:   all elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   interactive

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `transitionTimingFunction`

Percentages
:   N/A

## Syntax

-   `transition-timing-function: cubic-bezier()`
-   `transition-timing-function: steps()`
-   `transition-timing-function: ease`
-   `transition-timing-function: ease-in`
-   `transition-timing-function: ease-in-out`
-   `transition-timing-function: ease-out`
-   `transition-timing-function: linear`
-   `transition-timing-function: step-end`
-   `transition-timing-function: step-start`

## Values

ease
:   Default. Starts and stops gradually, equivalent to [**cubic-bezier(0.25,0.1,0.25,1)**](/css/functions/cubic-bezier)

linear
:   Starts and stops immediately, progressing at a constant rate, equivalent to [**cubic-bezier(0,0,1,1)**](/css/functions/cubic-bezier).

ease-in
:   Starts gradually and stops suddenly, equivalent to [**cubic-bezier(0.42,0,1,1)**](/css/functions/cubic-bezier).

ease-out
:   Starts suddenly and stops gradually, equivalent to [**cubic-bezier(0,0,0.58,1)**](/css/functions/cubic-bezier).

ease-in-out
:   Starts and stops gradually, equivalent to [**cubic-bezier(0.42,0,0.58,1)**](/css/functions/cubic-bezier).

[**cubic-bezier()**](/css/functions/cubic-bezier)
:   Function value specifying a customized response curve.

[**steps()**](/css/functions/steps)
:   Function value specifying a series of discrete intervals.

step-start
:   The change occurs instantly at the start of the keyframe, equivalent to [**steps(1, start)**](/css/functions/steps).

step-end
:   The change occurs instantly at the end of the keyframe, equivalent to [**steps(1, end)**](/css/functions/steps).

## Examples

Default transition timing

``` css
transition-timing-function: ease;
```

[A series of elements animate in progression. View live example](http://letmespellitoutforyou.com/samples/transit_delay.html)

No easing behavior: animation starts and stops abruptly and proceeds at a constant rate.

``` css
transition-timing-function: linear;
```

[View live example](http://letmespellitoutforyou.com/samples/transit_delay.html)

See how changing the timing value affects a sequence of two transitions

```

```

[View live example](http://letmespellitoutforyou.com/samples/transit_timing.html)

## Usage

     Along with other transition properties, multiple values

separated by commas apply to transitions in the same order as they are listed by the [**transition-property**](/css/properties/transition-property) property. Excess values are ignored. If there are fewer timing values than transitions, they're recycled in order of declaration until their numbers match.

## Related specifications

[CSS Transitions](http://www.w3.org/TR/2009/WD-css3-transitions-20091201/)
:   W3C Working Draft
