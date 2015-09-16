---
title: 'animation-play-state'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/7044978'
compatibility:
  feature: animation-play-state
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`running`'
  'Applies to': 'All elements, ::before and ::after pseudo-elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Defines whether an animation is running or paused.'
tags:
  - CSS
  - Properties
uri: css/properties/animation-play-state

---
## Summary

Defines whether an animation is running or paused.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `running`

Applies to
:   All elements, ::before and ::after pseudo-elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `animation-play-state: paused`
-   `animation-play-state: running`

## Values

running
:   Plays the animation. If restarting a paused animation, the animation resumes from the current (paused) state.

paused
:   Pauses the animation. A paused animation continues to display the current state of the animation.

## Examples

The CSS uses the animation property and the @keyframes property as well as the animation-play-state property and more.

The example show how to create a counter like function. By using the ":checked" selector for radio buttons we toggle the animation states for the counter

``` css
/* position the handles */
#stopwatch_handles {
    margin-top: 0px;
}
/* Style the labels itself, at the bottom we hide the radio buttons itself */
#stopwatch_handles label {
    cursor: pointer;
    padding: 5px 5px;
    font-family: Verdana, sans-serif;
    font-size: 12px;
}
input[name="handles"] {display: none;}

/*Actual handles  this triggers the stopwatch to start and stop based on the state of the radio buttons */
#stopbtn:checked~.stopwatch .numbers {
    animation-play-state: paused
}
#startbtn:checked~.stopwatch .numbers {
    animation-play-state: running
}

/* we set the animation in 10 steps of 1 second, and set the play state to paused by default */
.moveten {
    animation: moveten 1s steps(10, end) infinite;
    animation-play-state: paused;
}
/* here we do the same except for six */
.movesix {
    animation: movesix 1s steps(6, end) infinite;
    animation-play-state: paused;
}

/* here we actualy set the duration of the seconds so that they sync up when needed */
.second {
    animation-duration: 10s;
}
.tensecond {
    animation-duration: 60s;
}

/* and here are the keyframes so that the numbers animate vertically
The height is 30 and the there are 10 digits so to move up we use -300px (30x10) */
@keyframes moveten {
    0% {top: 0;}
    100% {top: -300px;}
}

/* The same goes for this one but instead of ten we have 6 so we get 30x6 = 180px */
@keyframes movesix {
    0% {top: 0;}
    100% {top: -180px;}
}
```

A mobile-like interface featuring a keyframe-animated pulsing icon. When the application enters an interruption mode, the icon is paused and the page presents another panel to indicate that the animation is inactive.

``` css
div.selected {
    animation: pulse 0.5s infinite alternate running;
}

body.interrupt div.selected {
    animation-play-state: paused;
}

@keyframes pulse {
    from {
        transform : scale(1) translateX(0);
        opacity : 1;
    }
    to {
        transform : scale(0.75) translateX(0);
        opacity : 0.25;
    }
}
```

[View live example](http://code.webplatform.org/gist/7044978)

## Usage

     Can also be a comma-separated list of play states, e.g., running, paused, running, where each play state is applied to the corresponding ordinal position value of the animation-name property.

## Related specifications

[CSS Animation](http://www.w3.org/TR/css3-animations/)
:   W3C Working Draft

## See also

### Other articles

-   [Making things move with CSS3 animations](/tutorials/css_animations)
-   [@keyframes](/css/atrules/@keyframes)
-   [animation](/css/properties/animation)
-   [animation-delay](/css/properties/animation-delay)
-   [animation-direction](/css/properties/animation-direction)
-   [animation-duration](/css/properties/animation-duration)
-   [animation-fill-mode](/css/properties/animation-fill-mode)
-   [animation-iteration-count](/css/properties/animation-iteration-count)
-   [animation-name](/css/properties/animation-name)
-   [animation-timing-function](/css/properties/animation-timing-function)
