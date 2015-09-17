---
title: 'Graceful Degradation'
notes:
  - "* Needs topics like \"concept\" or \"methodology\".\n Code-Block in second example doesn't work as expected (some lines missing: source tags doen't show up)"
readiness: 'In Progress'
summary: 'Graceful degradation, also known as Fault tolerance is a concept of building a web site or application so it provides a good level of user experience in modern browsers.'
tags:
  - Concept_Pages
uri: 'concepts/graceful degradation'

---
## Summary

Graceful degradation, also known as Fault tolerance is a concept of building a web site or application so it provides a good level of user experience in modern browsers.

 However, it will degrade *gracefully* for those using older browsers. The system may not be as pleasant or as pretty, but the basic functionality will work on older systems.

> [..] Graceful Degradation is the journey from complexity to simplicity

[@smashingmag](http://www.smashingmagazine.com/2009/04/22/progressive-enhancement-what-it-is-and-how-to-use-it/)

You start creating your website or web-application with the use of features that are available in the latest generation of modern browsers. Thereafter, have a look on older browsers and systems and start creating fallbacks by using [polyfills](/concepts/polyfill) or other workarounds.

## Examples

**Definition of Done:** Create a videoplayer that is working on IE6 up to IE10.

Cause you trust the approach of GD, you prefer the HTML5 `<video>` tag over Flash as your entry point. Now your videoplayer works well on IE9 & 10. You need to create a fallback for IE6-8, that does not support HTML5Video. You'll now create another instance of your player based on Flash, which is a graceful replacement of your HTML5 player.

``` html
<video>



```

     <object id="flash_fallback_1" type="application/x-shockwave-flash" data="player.swf">
       <param name="movie" value="video.mp4" />
     </object>

\</video\>

</pre>

## See also

### External resources

-   [W3C: Graceful degredation versus progressive enhancement](http://www.w3.org/wiki/Graceful_degredation_versus_progressive_enhancement)
-   [Wikipedia: Fault tolerance](http://en.wikipedia.org/wiki/Fault_tolerance)
