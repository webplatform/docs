---
title: Polyfills for Replicating Web APIs
readiness: 'In Progress'
summary: 'Polyfills replicate browser-native APIs, so that code dependent on provided endpoints can be run in browsers that don''t have them.'
tags:
  - Concept
  - Pages
  - Compatibility
  - JavaScript
uri: concepts/polyfill

---
## Summary

Polyfills replicate browser-native APIs, so that code dependent on provided endpoints can be run in browsers that don't have them.

 The term "polyfill" was initially coined by Remy Sharp in 2009. Polyfills are drop-in libraries that intend to seamlessly fill browser capability gaps. "Seamlessly" meaning that they mimic the interface of the capability they are replicating as close as possible.

In addition to polyfills there also exists the category of "shims". Similar to polyfills shims also intend to bring additional capability to a browser. But they do that exposing their own proprietary interface, not replicating the official one.

Both allow you to target and tinker around with new technology which is not yet available across all commonly used browsers. So you could for example polyfill the Geolocation API in all the older IEs and then build your site around some Geolocation goodness without the IE users being left behind.

The main difference and advantage between the two types of libraries is that with polyfills you can write your code against the official spec and then just slap in the library when a browser happens to not (yet) support it. Usually you use a so called "feature detection" to find that out. Most libraries document how to do that. Then, after a certain period of time during which people upgrade to newer browser versions, the need for the polyfill vanishes - up to the point where you can safely remove it from your code.

## Examples

Remy Sharp's [localStorage polyfill](https://gist.github.com/350433). This simulates the Web Storage API so that (typically older) browsers can successfully execute code that depends on it.

It basically loads the polyfill if there is no `localStorage` property on the `window` object.

``` html
<script>
// If a browser does not support localStorage, load the polyfill
var polyfill;
if (!window.localStorage) {
        polyfill = document.createElement('script');
        polyfill.type = 'text/javascript';
        polyfill.src = 'localStorage.js';
        document.getElementsByTagName('head')[0].appendChild(polyfill)
}
</script>
```

You can detect the support of SVG images in a browser and polyfill non-supporting browsers with a PNG fallback image. This example uses a [Modernizr](http://modernizr.com/) test for SVG support.

``` css
.site-logo {
    background: url('logo.svg') no-repeat 0 50%;
}

.no-svg .site-logo {
    background-image: url('logo.png');
}
```

## See also

### External resources

-   [Explanation on Wikipedia](http://en.wikipedia.org/wiki/Polyfill)
-   [Remy Sharp - "What is a Polyfill"](http://remysharp.com/2010/10/08/what-is-a-polyfill/)
-   [Modernizr's mighty "HTML5 Cross Browser Polyfills" list](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills)
-   [HTML5 Please's list of HTML5 features usable cross-browser with polyfills](http://html5please.com/#polyfill)
