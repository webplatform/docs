---
title: 'Touch Input Considerations'
readiness: 'In Progress'
summary: 'Today''s mobile devices are exploding in popularity, and most of them have capacitive touch screens, which provide input affordances that are very different from keyboard-and-mouse interfaces.  When the web was being developed, the vast majority of computers had a keyboard and mouse attached. Thus, the web provided (and continues to provide) a rich API for handling these sorts of input events.'
tags:
  - Concept_Pages
  - Needs_Examples
uri: 'concepts/mobile web/touch'

---
## Summary

Today's mobile devices are exploding in popularity, and most of them have capacitive touch screens, which provide input affordances that are very different from keyboard-and-mouse interfaces. When the web was being developed, the vast majority of computers had a keyboard and mouse attached. Thus, the web provided (and continues to provide) a rich API for handling these sorts of input events.

## Conceptual differences between mouse and touch

Today's mobile devices are exploding in popularity, and most of them have capacitive touch screens, which provide input affordances that are very different from keyboard-and-mouse interfaces:

-   Coarse input (fat fingers vs. tiny mouse pointers)
-   Multiple pointers
-   No hover events

When the web was being developed, the vast majority of computers had a keyboard and mouse attached. Thus, the web provided (and continues to provide) a rich API for handling these sorts of input events, as described in the [mouse and keyboard events](http://www.google.com) article.

With the advent of touch screens, the web had to adapt, and eventually the touch events were developed and implemented in mobile web browsers.

## Touch events on the web

The basic touch events of the web are:

-   `touchstart`, which corresponds to a new finger being placed on the touchscreen.
-   `touchmove`, which corresponds to a finger moving across the screen.
-   `touchend`, which corresponds to a finger lifting from the screen.
-   `touchenter`, which corresponds to a moving finger already on the screen entering a target.
-   `touchleave`, which corresponds to a moving finger already on the screen leaving a target.

Each of these events contains a list of touches, with a numeric identifier associated with each touch. The [basic touch events](http://www.google.com) article describes this model in greater detail.

## Demystifying the click event

When the click event was conceived (before touch screens became popular), it was intended as a high level event to describe a mouse press followed by a mouse release in roughly the same area of the screen.

On touch screens, click behaves more like a tap. The main difference here stems from the fact that fingers are far less precise than mouse pointers. As a result, some browsers like Chrome for Android do touch adjustments which scores all nodes underneath the finger (using radius information if available from the hardware) and picks the best one. This is very different from just using the `touchdown` event, which taps on the first element only using the center of the touch point.

## Building sites for both mouse and touch input

Though the mouse is still a very common input modality, increasingly, the web is being viewed on touch screens. This means that we need to build sites that work well for both mouse and touch. Furthermore, some devices (eg. Windows 8 Surface) let you use both kinds of input by providing a touch screen and a physical keyboard. It is not safe to assume that just because a device has touch support, it doesn't have mouse input, and vice versa.

Because of this complex landscape, it's important to do proper feature detection. New media queries have been proposed around the coarseness of the input (pointer: course |1)\_ In general, feature detection is best handled by an external library like [Modernizr](http://modernizr_com), since feature detection approaches vary between browsers and browser versions, and are constantly in flux\_

Because many web pages were not originally developed for devices with touch screens, browsers implement a fallback to mouse events\_ If a user taps some element on a touch screen, in addition to triggering a touch event, the browsers will pretend as if there was also a mouse event, and relay it to the page\_ This behavior is described in more detail in the synthetic mouse events article\_ You can also prevent the associated [synthetic mouse events](http://www_google_com) from firing by calling `event_prentDefault()` in your touch handlers\_==Touch performance considerations== Beware of the infamous 300ms click delay in many mobile web browsers. This delay exists because in many cases, double tapping the screen causes the page to zoom. After each tap, the browser cannot fire a click event until it is certain that there was no follow up touch event (which would indicate a zoom). This behavior causes a visible delay before the resulting event is fired. This can be remedied by using one of many [fast click](http://www.google.com) approaches which use raw touch events, or in some newer browsers by [setting the viewport](http://www.google.com) to never scale.

Scrolling is another tricky area for performance. Mobile devices often feature inertial scrolling, where moving a finger on the screen and then releasing it causes the scrolled content to continue scrolling in the same direction. This effect is provided by a [variety of JavaScript libraries](http://www.google.com), but incurs significant performance overhead. The web platform provides some optional scrolling optimizations as well, which are described in more detail in [optimizing scrolling](http://www.google.com) performance.

Finally, handling large amounts of multi-touch input can be very taxing because of the high frequency of `touchmove` events that results from many fingers being on the screen simultaneously. It's important to decouple drawing and input handling in this cases.

## Higher level gestures

Touch screens unlock the possibility of interesting multi-touch gestures, the best known of which is pinch-zoom, often used for zooming content. Unfortunately, this area is heavily laden with patents, leading to an uneven landscape of support across the different browsers. iOS devices provide [Safari high level gesture events](http://www.google.com), and there are [a number of JavaScript libraries](http://www.google.com) that implement gestures on top of the raw touch events.

## Touching developer tools

Debugging input on mobile devices can be challenging because of the overhead of dealing with multiple devices. Though nothing can really replace testing on the actual device you are targeting, it can make sense to start by using tools to simulate a touch environment on the desktop. The Chrome DevTools provide a way to emulate touch events, essentially pre-translating every mouse event into the equivalent touch one (eg. `mousedown` becomes `touchstart`). This is useful for debugging single-touch applications. For more complex interactions, multi-touch can also be simulated (with projects like [MagicTouch](http://www.google.com)), given the appropriate setup.

With remote debugging in the Chrome DevTools, you can also set up event listener breakpoints that will break whenever a user performs touch-based interactions with the desired element. For more information on these techniques, see the [mobile developer tools](http://www.google.com) article.

## A consolidated model

Despite the many differences between the two input modes, mouse and touch input is fundamentally similar in one way: both fingers and mouse pointers can be viewed as abstract points with screen coordinates. This similarity makes it tempting to consolidate the two disparate models into one, which just deals with lists of pointers. This model was first proposed by Microsoft in the [pointer events specification](http://www.google.com). Though not implemented in the web platform yet, several [pointer event polyfills](http://www.google.com) exist in the wild.

A consolidated pointer-based model makes it easier to build sites that work well for both mouse and touch, avoiding click delays but still making it as easy to write multi-touch gestures if needed.

## See also

### Related articles

#### Touch

-   **Touch Input Considerations**

-   [touch](/css/touch)

