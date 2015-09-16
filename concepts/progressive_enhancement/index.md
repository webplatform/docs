---
title: Progressive Enhancement
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
  - 'Portions of this content come from HTML5Rocks!.'
code_samples:
  - 'http://css-tricks.com/examples/RGBaSupport/'
notes:
  - "* Needs topics like \"concept\" or \"methodology\".\n Code-Block in second example doesn't work as expected (some lines missing)"
readiness: 'Almost Ready'
summary: 'Progressive enhancement is a powerful development philosophy for creating universally accessible sites and web apps. It does require some learning, experience and discipline, but the return of investment is high.'
tags:
  - Concept
  - Pages
  - Compatibility
  - CSS
  - Design
  - HTML
  - JavaScript
uri: 'concepts/progressive enhancement'

---
## Summary

Progressive enhancement is a powerful development philosophy for creating universally accessible sites and web apps. It does require some learning, experience and discipline, but the return of investment is high.

 Part of the appeal of PE is the strength of the end result. PE forces you to initially plan out your project as a functional system using only the most basic of Web technologies. This means that you know you’ll always have a strong foundation to fall back on. You start by establishing a basic level of user experience that all browsers will be able to provide when rendering your web site, but you also build in more advanced functionality that will automatically be available to browsers that can use it.

## The Layers of Progressive Enhancement

In practical terms, it’s easiest to break the concept of PE into different layers, each one building on the previous to improve the experience of interacting with the website.

-   **Markup** The first layer is clean, semantic HTML. This allows text-based, speech-based, antiquated and robotic user-agents to navigate the content of your website properly.
-   **Styling** The second layer is CSS. This allows visual-based user-agents to display or alter the visual representation of your website’s content.
-   **Behavior** The third layer is JavaScript. This allows user-agents that are capable of using it to provide your users with enhanced usability.

There is another concept called [**Graceful Degradation**](/concepts/graceful_degradation) (GD), what you should know. GD is similar, but it is an older concept *(predecessor of progressive enhancement)* that does things the other way round.

## Examples

RGBa is not supported in all Browsers, so we have to declare a fallback color. Not declaring a fallback means no color will be applied in browsers that don't support it.

``` css
div {
   background: red; /* The Fallback */
   background: rgba(200, 54, 54, 0.5);
}
```

[View live example](http://css-tricks.com/examples/RGBaSupport/)

`requestAnimationFrame` provides a native API for running any type of animation in the browser. How to use it the progressive enhanced way? *Avoid browser-specific code and use feature detection (not browser detection)*

``` js
// Crossbrowser animation
var requestAnimation = (function() {
  return window.requestAnimationFrame
```

## See also

### External resources

-   [Overview and Best Practices](http://sixrevisions.com/web-development/progressive-enhancement/)
-   [What It Is, And How To Use It?](http://www.smashingmagazine.com/2009/04/22/progressive-enhancement-what-it-is-and-how-to-use-it/)
