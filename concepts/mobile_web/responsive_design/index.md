---
title: 'Responsive Web Design'
readiness: 'Ready to Use'
summary: 'Responsive Web Design is an approach that emphasises design which works well across a variety of devices and browsing contexts -- without serving different content for each different operating system, device, browser, display size or pixel density.'
tags:
  - Concept_Pages
  - Design
  - Mobile
  - UI
  - Usability
uri: 'concepts/mobile web/responsive design'

---
## Summary

Responsive Web Design is an approach that emphasises design which works well across a variety of devices and browsing contexts -- without serving different content for each different operating system, device, browser, display size or pixel density.

 Responsive Web Design (RWD for short) is an approach that emphasises design which works well across a variety of devices and browsing contexts -- without serving different content for each different operating system, device, browser, display size or pixel density.

[](/File:marcotte.jpg)

Ethan Marcotte's article for A List Apart

![Ethan Marcotte's article for A List Apart](/assets/thumb/b/b9/marcotte.jpg/400px-marcotte.jpg)

The term was coined by Ethan Marcotte in [an article on A List Apart](http://www.alistapart.com/articles/responsive-web-design/), who suggested three methods to cope with different browser window sizes:

-   Fluid grids (layout that adjusts to fit the viewport)
-   Flexible images (images that [adjust to fit](http://www.alistapart.com/articles/dao/))
-   CSS [Media Queries](http://css-tricks.com/css-media-queries/)

To get a sense of what RWD means it's best to see it in action. There are lots of examples of sites using responsive design at [mediaqueri.es](http://mediaqueri.es/): open the sites listed on mediaqueri.es in a desktop browser and try resizing the browser window.

Earlier web designers had discovered the advantages of [separating content from layout](http://csszengarden.com/) as well as using [liquid layout](http://www.maxdesign.com.au/articles/liquid/) and [hybrid techniques](http://coding.smashingmagazine.com/2009/06/02/fixed-vs-fluid-vs-elastic-layout-whats-the-right-one-for-you/) as opposed to static, 'pixel perfect' attempts to mimic Photoshop and print media. As John Allsopp wrote in [The Dao of Web Design](http://www.alistapart.com/articles/dao/): 'Now is the time for the medium of the web to outgrow its origins in the printed page.'

Jared Ponchot points out that [the web was by it's very nature designed to be responsive](http://www.lullabot.com/articles/responsive-adaptive-web-design).

### The perils of serving different content

[](/File:mobile_book.jpg)

Smashing Mobile Book

![Smashing Mobile Book](/assets/public/c/c3/mobile_book.jpg)

Maintaining a parallel 'mdot' website for mobile platforms -- for example, serving m.webplatform.org to mobile devices and www.webplatform.org to desktop browsers -- can incur significant overheads for code management, content synchronisation and hosting infrastructure.

Even if you only have one site, but you serve different content to different devices, you always risk alienating someone. Trent Walton gives a good example of this in the [Smashing Mobile Book](http://www.smashingmagazine.com/the-mobile-book): his favourite news website removed the pollen report from its mobile version, which was the information that meant most to him. The moral of this tale is: best not to guess what content or features your users won't miss.

Consistent content is king! Responsive design can be used to give all your users access to all your site's or app's content and features.

## Workflow and process

[](/File:responsive_comping.jpg)

Responsive Comping article by Matt Griffin

![Responsive Comping article by Matt Griffin](/assets/thumb/6/6c/responsive_comping.jpg/300px-responsive_comping.jpg)

For RWD to work, everyone involved in the production process must collaborate, including designers, coders, writers, illustrators and business managers. Different workers have may have different skills, but good design has to be holistic.

Web content is consumed via an increasing variety of software and hardware, with different display sizes, input methods and usage contexts. This means that style guides should avoid fixed sizes and positioning. Trent Walton refers to this new way of method of design as 'a network of content that can be rearranged at any screen size to best convey the message'.

A simple way to start on responsive design is to ensure that design begins with 'lo-fi' mockups and benefits from [discount usability](http://www.useit.com/alertbox/discount-usability.html) testing. There are [lots of](http://www.netmagazine.com/features/50-fantastic-tools-responsive-web-design)[tools](http://www.netmagazine.com/features/50-fantastic-tools-responsive-web-design) to help achieve this. (Other prototyping tools include [Ratchet](http://maker.github.com/ratchet/) and [Foundation](http://foundation.zurb.com/).) Applications such as [Balsamiq Mockups](http://www.balsamiq.com/products/mockups) make it possible to quickly try out interface ideas, without producing pixel perfect printouts that would encourage static designs.

Developer Brad Frost has compiled a [list of resources](http://bradfrost.github.com/this-is-responsive/resources.html#process) for implementing a responsive design process.

To make RWD possible in a commercial context, it is crucial to be able to get sign-off for responsive designs: Matt Griffin has suggestions on how to achieve this in his article about what he calls [responsive comping](http://www.alistapart.com/articles/responsive-comping-obtaining-signoff-with-mockups/).

## Layout, sizing and grids

### Viewport

There are two types of width specified in the context of browser display space:

-   `device-width`: the width of the display (the 'desktop')
-   `width`: the width of the browser viewport.

However, most smartphone browsers actually use a nominal display 'viewport' which is wider than the width of the device, and set `width` to be the width of the viewport. In other words, the browser displays web content in a 'window' that may be wider than the actual device, and the user can then swipe or zoom to navigate between on- and off-screen web page content. This is done to ensure that unresponsive sites aren't crammed into the device width, which is a sensible compromise, but can cause problems for responsive design since it means that the device size doesn't correspond to the virtual viewport size.

To get around this, Apple devised a simple solution: the viewport meta element:

`<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0">`

This example causes `width` to equal `device-width`: the 'window' that web content is displayed in has the same dimensions as the actual display. (The scale values refer to zoom level.)

A [comprehensive guide to the viewport meta element](https://developer.mozilla.org/en-US/docs/Mobile/Viewport_meta_tag) is available on the Mozilla Developer Network, and there are a number of [tools for viewport testing](http://bradfrost.github.com/this-is-responsive/resources.html#viewport-testing).

### Dimensions and units

#### A pixel is not a pixel

One of the major problems with using px (pixel) units on mobile devices is that a 'CSS pixel' (the unit used in a CSS rule) may not correspond to a 'device pixel' (the actual coloured dot on the display). This number of device pixels per unit of physical width is referred to as [pixel density](http://en.wikipedia.org/wiki/List_of_displays_by_pixel_density). (To determine the appropriate resolution for an image in a given context, the browser uses the device pixel ratio, as described in Boris Smus's [article about high-DPI images](http://www.html5rocks.com/en/mobile/high-dpi/#toc-calculating-dpr) explains the meaning of device pixel ratio.)

[](/File:device_pixel_ratio.png)

A diagram showing one reference angular pixel, to help illustrate how devicePixelRatio is calculated

![A diagram showing one reference angular pixel, to help illustrate how devicePixelRatio is calculated.](/assets/thumb/3/37/device_pixel_ratio.png/400px-device_pixel_ratio.png)

Browser vendors such as Apple and Mozilla found that sites displayed poorly on high-resolution devices (i.e. those with a high density of physical pixels) if browsers kept to a one-to-one ratio between CSS pixels and device pixels. As a result, this ratio varies across browsers and platforms.

This means that, unlike for print media, it is not advisable to attempt to specify absolute (physical) size for text, images or layout on the web. Peter Paul Koch has written a [very detailed guide](http://www.quirksmode.org/blog/archives/2010/04/a_pixel_is_not.html) to this problem. Zoom compounds the situation: for more information, see [High DPI sites](https://www.webkit.org/blog/55/high-dpi-web-sites/) on the Surfin' Safari blog, and the Quirksmode post, [A tale of two viewports](http://www.quirksmode.org/mobile/viewports.html).

As a result, one of the core techniques of responsive design is to use relative, not absolute units, and techniques for this are described throughout Koch's article.

## Media queries

CSS media queries allow you to choose different CSS rules for different browsing conditions, such as media (print or screen), display width or device orientation. Media queries are at the core of RWD approaches, because they enable web designers to specify different layouts and sizes for different contexts.

You can use media queries to apply different stylesheets:

    <link rel='stylesheet' media='screen and (min-width: 400px) and (max-width: 800px)' href='css/smallish.css' />

...or different rules:

    @media all and (min-width: 300px) and (max-width: 600px) {
      header {
        background-image: url(bg_small.png);
        padding: 0.5em;
      }
    }

[mediaqueri.es](http://mediaqueri.es/) provides examples of sites that use media queries, Mozilla Developer Network provides [a detailed reference to media queries](https://developer.mozilla.org/en-US/docs/CSS/Media_queries), and more details of features that may be implemented in the future are available from the [W3C Recommendation](http://www.w3.org/TR/css3-mediaqueries/).

#### Breakpoints

[](/File:mediaqueri.es.png)

mediaqueri.es site

![mediaqueri.es site](/assets/thumb/d/db/mediaqueri.es.png/400px-mediaqueri.es.png)

'Breakpoint' is CSS-speak for the dimensions at which a different sets of style rules should be applied. Layout are liable to 'break' at particular sizes: for example, two 350px-wide images side by side with no padding or margin might overlap horizontally when the width of the viewport goes below 700px.

There are two ways to work out breakpoints:

-   By device size, [using common dimensions](http://www.html5rocks.com/en/mobile/cross-device/#toc-client-detect) for (say) phones, tablets, laptops and larger screens.
-   Based on content, adding breakpoints at dimensions that make sense for your layouts.

The problem with the device-size approach is that the number of device types and sizes is continually changing, and boundaries are getting blurred. This makes it hard to maintain the 'right' device-oriented breakpoints. In general it may make more sense to add breakpoints to suit content, so layouts don't 'break' no matter what size the screen.

It's easy to test this out, with tools like Remy Sharp's [responsivepx](http://responsivepx.com/) and Brad Frost's [ish](http://bradfrostweb.com/blog/post/ish/).

#### Responsive design v Adaptive design v adaptive layout

[Adaptive web design](http://blog.easy-designs.net/archives/2011/11/16/on-adaptive-vs-responsive-web-design/) can respond to varying contexts without fluid grids and flexible images, for example by providing different page components in different contexts. Brad Frost [gives three examples](http://blog.easy-designs.net/archives/2011/11/16/on-adaptive-vs-responsive-web-design/) of design that is adaptive rather than responsive:

Can this device access my location? If so, inject a Use Current Location button onto the site in addition to the basic store-finder form.

Does this device understand touch events? If so, make this image carousel swipeable in addition to the previous and next buttons.

Does the browser support HTML5 canvas? If so, replace this static image with a canvas element.

For typography, images and layout, adaptive design might respond to breakpoints in a way that is not 'responsive': for example, by using fixed measures rather than fluid grids.

'Adaptive design' also refers more generally to the idea of [progressive enhancement](http://en.wikipedia.org/wiki/Progressive_enhancement): for example, providing location-based functionality for a web app on mobile devices, but not on the desktop.

The differences between 'adaptive' and 'responsive' have been summarised by [Aaron Gustafson](http://blog.easy-designs.net/archives/2011/11/16/on-adaptive-vs-responsive-web-design/), often credited with inventing the term 'adaptive design'. Marc ven den Dobbelsteen also used the term 'adaptive design' in his 2006 [Switch McLayout article](http://www.alistapart.com/articles/switchymclayout). Brad Frost [has suggested](http://blog.easy-designs.net/archives/2011/11/16/on-adaptive-vs-responsive-web-design/) that responsive design is a subset of adaptive design.

#### More information

Using media queries on mobile platforms: <http://mobile.smashingmagazine.com/2010/07/19/how-to-use-css3-media-queries-to-create-a-mobile-version-of-your-website/>

Reference: [developer.mozilla.org/en-US/docs/CSS/Media\_queries](https://developer.mozilla.org/en-US/docs/CSS/Media_queries)

W3C Recommendation: [w3.org/TR/css3-mediaqueries](http://www.w3.org/TR/css3-mediaqueries/)

## Testing

[](/File:responsivepx.png)

Remy Sharp's responsivepx tool

![Remy Sharp's responsivepx tool](/assets/thumb/c/ce/responsivepx.png/500px-responsivepx.png)

For responsive design to work well, it is especially important to test sites and applications at different viewport sizes.

Remy Sharp's [responsivepx](http://responsivepx.com/?simpl.info#640x480&scrollbars) makes it possible to adjust viewport width and height values, in order to find the [breakpoints](https://docs.google.com/a/google.com/document/d/1wciRNw81BdIbuwzJJzcGJVhzkOvm1AZwS0KgULZAiZw/edit#heading=h.umsakrrk7jlc) at which responsive layouts need to change.

[](/File:ish.png)

Brad Frost's ish resizer

![Brad Frost's ish resizer](/assets/thumb/9/9f/ish.png/500px-ish.png)

Brad Frost's [ish](http://bradfrostweb.com/demo/ish/) resizer emphasises that breakpoints should be based on content rather than nominal device dimensions.

 For responsive typography, [designers have found](http://www.webtypography.net/Rhythm_and_Proportion/Horizontal_Motion/2.1.2/) that body text should generally have between 45 and 75 characters per line. A simple trick for testing layouts [suggested by Trent Walton](http://trentwalton.com/2012/06/19/fluid-type/), is to add an asterisk to lorem text after 45 and 75 characters. If both asterisks appear on the same line at a particular viewport width, the font size needs to be changed.

A huge range of other tools is available for testing and debugging responsive design components including images, fonts and layouts. For more information and resources see the [Mobile Debugging article](/concepts/internet_and_web/html5_hybrid_applications/concepts/mobile_debugging#Devices) on webplatform.org.

## Pro and con

A word of warning: 'pure' RWD may not always be appropriate, and developers such as Guy Podjarny have pointed to [potential performance problems](http://guypo.com/technical/responsive-web-design-is-bad-for-performance-there-i-said-it).

In [5 Reasons Why Responsive Design Is Not Worth It](https://managewp.com/5-reasons-why-responsive-design-is-not-worth-it/comment-page-1) Tom Ewer argues that RWD is simply a waste of time and money given that modern mobile browsers are designed to cope well with non-responsive sites (for example, by zooming elements to full width when they're tapped on). Ewer also suggests that providing different layouts for different browsing contexts is confusing to users.

Developers have encountered several other RWD hazards:

-   Embedded components such as maps or games may not translate well to responsive designs
-   Users may prefer the 'swipe and zoom' approach: getting a visual overview of a site, then zooming in to what interests them
-   Providing different site layouts on different platforms might surprise users -- reducing trust, recognition and consistency -- even if site content is the same
-   Website publishers need to monetize their sites and apps, and [many ads are not responsive](http://www.netmagazine.com/features/state-responsive-advertising-publishers-perspective).
-   Many developers have to work with existing code and content, and cannot not start from scratch. In this case [hybrid approaches may be a better bet](http://simplebits.com/notebook/2011/08/19/adapted/).
-   Older browsers do not support media queries, CSS properties such as `max-width` and may not even support techniques such as relative sizing (or even have good support for fixed sizing). This can be a particular problem for the significant minority of browsers on low-end cellphones.

Some techniques for dealing with these issues are described below.

### Coping with older browsers

#### Media queries

Scott Jehl's [Respond.js polyfill](https://github.com/scottjehl/Respond) enables min-width and max-width rules, even with older browsers such as Internet Explorer 6 8; [jQuery](http://www.jquery.com/) likewise.

#### Feature detection

The [Modernizr](http://www.modernizr.com/) library works on most web platforms and can be used to build responsive sites and apps which work in a range of contexts.

#### Polyfills

A polyfill (think [Polyfilla](http://www.wilkinsonplus.com/content/ebiz/wilkinsonplus/invt/0288365/0288365_l.jpg)) is code that enables features to be used natively, if they're available, or replicates them if they're not. This can be very useful for achieving future-proof RWD across a range of browsers.

### High performance RWD

Several developers have suggested techniques to avoid or minimise performance problems with RWD.

Guy Podjarny: [Responsive Web Design Makes It Hard To Be Fast](http://guypo.com/technical/responsive-web-design-is-bad-for-performance-there-i-said-it) and [Performance Implications of Mobile Design](http://www.slideshare.net/guypod/performance-implications-of-mobile-design-perf-audience-edition)

Jason Grigsby: [The Performance Implications of Responsive Web Design](http://lanyrd.com/2012/velocity/stpqq/)

Brad Frost: list of RWD [performance resources](http://bradfrost.github.com/this-is-responsive/resources.html#performance)

### RWD opt out

[](/File:bruce_lawson.png)

Bruce Lawson blog post: opting out of RWD

![Bruce Lawson blog post: opting out of RWD](/assets/thumb/e/e9/bruce_lawson.png/300px-bruce_lawson.png)

Bruce Lawson and other developers have suggested that it might be appropriate to give users the option to opt out of RWD: his [blog post](http://www.brucelawson.co.uk/2013/turning-off-responsive-web-design/) on the subject, has links to articles explaining techniques for enabling this.

## Further reading

[Responsive Web Design](http://www.alistapart.com/articles/responsive-web-design/), by Ethan Marcotte

[This is Responsive](http://bradfrost.github.com/this-is-responsive/): patterns, resources and news collated by Brad Frost

[The Dao of Web Design](http://www.alistapart.com/articles/dao/): influential article by John Allsopp from April 2000: 'Now is the time for the medium of the web to outgrow its origins in the printed page.'

[A List Apart articles on responsive design](http://www.alistapart.com/articles/)

## Related concepts

Adaptive web design

[Progressive enhancement](http://en.wikipedia.org/wiki/Progressive_enhancement)

[Liquid layout](http://coding.smashingmagazine.com/2009/06/02/fixed-vs-fluid-vs-elastic-layout-whats-the-right-one-for-you/)

## See also

### Related articles

#### CSS Layout

-   **Responsive Web Design**

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

#### Grid Layout

-   **Responsive Web Design**

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-column-position](/css/properties/grid-column-position)

-   [grid-column-span](/css/properties/grid-column-span)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [grid-row-position](/css/properties/grid-row-position)

-   [height](/css/properties/height)

#### Media Queries

-   **Responsive Web Design**

-   [\<resolution\>](/css/data_types/resolution)

-   [accelerator](/css/media_queries/accelerator)

-   [MediaQueryList](/css/media_queries/apis/MediaQueryList)

-   [MediaQueryListListener](/css/media_queries/apis/MediaQueryListListener)

-   [StyleMedia](/css/media_queries/apis/StyleMedia)

-   [addListener](/css/media_queries/apis/addListener)

-   [handleChange](/css/media_queries/apis/handleChange)

-   [matchMedia](/css/media_queries/apis/matchMedia)

-   [matchMedium](/css/media_queries/apis/matchMedium)

-   [matches](/css/media_queries/apis/matches)

-   [media](/css/media_queries/apis/media)

-   [type](/css/media_queries/apis/properties/type)

-   [removeListener](/css/media_queries/apis/removeListener)

-   [Colors by](/css/media_queries/colors_by)

-   [device-height](/css/media_queries/device-height)

-   [filter](/css/media_queries/filter)

-   [ms-interpolation-mode](/css/media_queries/ms-interpolation-mode)

-   [behavior](/css/properties/behavior)
