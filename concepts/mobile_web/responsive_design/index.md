{{Page_Title|Responsive Web Design}}
{{Flags}}
{{API_Name}}
{{Summary_Section|Responsive Web Design is an approach that emphasises design which works well across a variety of devices and browsing contexts -- without serving different content for each different operating system, device, browser, display size or pixel density.}}
{{Concept_Page
|Content=Responsive Web Design (RWD for short) is an approach that emphasises design which works well across a variety of devices and browsing contexts -- without serving different content for each different operating system, device, browser, display size or pixel density.

<div style="padding:10px 10px 10px 10px">
[[File:marcotte.jpg|thumb|left|400px|Ethan Marcotte's article for A List Apart|alt=Ethan Marcotte's article for A List Apart]]
</div>

The term was coined by Ethan Marcotte in [http://www.alistapart.com/articles/responsive-web-design/ an article on A List Apart], who suggested three methods to cope with different browser window sizes:

* Fluid grids (layout that adjusts to fit the viewport)
* Flexible images (images that [http://www.alistapart.com/articles/dao/ adjust to fit])
* CSS [http://css-tricks.com/css-media-queries/ Media Queries]

To get a sense of what RWD means it's best to see it in action. There are lots of examples of sites using responsive design at [http://mediaqueri.es/ mediaqueri.es]: open the sites listed on mediaqueri.es in a desktop browser and try resizing the browser window.

Earlier web designers had discovered the advantages of [http://csszengarden.com/ separating content from layout] as well as using [http://www.maxdesign.com.au/articles/liquid/ liquid layout] and [http://coding.smashingmagazine.com/2009/06/02/fixed-vs-fluid-vs-elastic-layout-whats-the-right-one-for-you/ hybrid techniques] as opposed to static, 'pixel perfect' attempts to mimic Photoshop and print media. As John Allsopp wrote in [http://www.alistapart.com/articles/dao/ The Dao of Web Design]: 'Now is the time for the medium of the web to outgrow its origins in the printed page.'

Jared Ponchot points out that [http://www.lullabot.com/articles/responsive-adaptive-web-design the web was by it's very nature designed to be responsive].

=== The perils of serving different content ===

[[File:mobile_book.jpg|thumb|300px|Smashing Mobile Book|alt=Smashing Mobile Book]]

Maintaining a parallel 'mdot' website for mobile platforms -- for example, serving m.webplatform.org to mobile devices and www.webplatform.org to desktop browsers -- can incur significant overheads for code management, content synchronisation and hosting infrastructure.

Even if you only have one site, but you serve different content to different devices, you always risk alienating someone. Trent Walton gives a good example of this in the [http://www.smashingmagazine.com/the-mobile-book Smashing Mobile Book]: his favourite news website removed the pollen report from its mobile version, which was the information that meant most to him. The moral of this tale is: best not to guess what content or features your users won't miss.

Consistent content is king! Responsive design can be used to give all your users access to all your site's or app's content and features.

== Workflow and process ==

[[File:responsive_comping.jpg|thumb|left|300px|Responsive Comping article by Matt Griffin|alt=Responsive Comping article by Matt Griffin]]

For RWD to work, everyone involved in the production process must collaborate, including designers, coders, writers, illustrators and business managers. Different workers have may have different skills, but good design has to be holistic.

Web content is consumed via an increasing variety of software and hardware, with different display sizes, input methods and usage contexts. This means that style guides should avoid fixed sizes and positioning. Trent Walton refers to this new way of method of design as 'a network of content that can be rearranged at any screen size to best convey the message'.

A simple way to start on responsive design is to ensure that design begins with 'lo-fi' mockups and benefits from [http://www.useit.com/alertbox/discount-usability.html discount usability] testing. There are [http://www.netmagazine.com/features/50-fantastic-tools-responsive-web-design lots of][http://www.netmagazine.com/features/50-fantastic-tools-responsive-web-design tools] to help achieve this. (Other prototyping tools include [http://maker.github.com/ratchet/ Ratchet] and [http://foundation.zurb.com/ Foundation].) Applications such as [http://www.balsamiq.com/products/mockups Balsamiq Mockups] make it possible to quickly try out interface ideas, without producing pixel perfect printouts that would encourage static designs.

Developer Brad Frost has compiled a [http://bradfrost.github.com/this-is-responsive/resources.html#process list of resources] for implementing a responsive design process.

To make RWD possible in a commercial context, it is crucial to be able to get sign-off for responsive designs: Matt Griffin has suggestions on how to achieve this in his article about what he calls [http://www.alistapart.com/articles/responsive-comping-obtaining-signoff-with-mockups/ responsive comping].

== Layout, sizing and grids ==

=== Viewport ===

There are two types of width specified in the context of browser display space:

* <tt>device-width</tt>: the width of the display (the 'desktop')
* <tt>width</tt>: the width of the browser viewport.

However, most smartphone browsers actually use a nominal display 'viewport' which is wider than the width of the device, and set <tt>width</tt> to be the width of the viewport. In other words, the browser displays web content in a 'window' that may be wider than the actual device, and the user can then swipe or zoom to navigate between on- and off-screen web page content. This is done to ensure that unresponsive sites aren't crammed into the device width, which is a sensible compromise, but can cause problems for responsive design since it means that the device size doesn't correspond to the virtual viewport size.

To get around this, Apple devised a simple solution: the viewport meta element:

<tt>&lt;meta name=&quot;viewport&quot; content=&quot;width=device-width, initial-scale=1.0, minimum-scale=1.0&quot;&gt;</tt>

This example causes <tt>width</tt> to equal <tt>device-width</tt>: the 'window' that web content is displayed in has the same dimensions as the actual display. (The scale values refer to zoom level.)

A [https://developer.mozilla.org/en-US/docs/Mobile/Viewport_meta_tag comprehensive guide to the viewport meta element] is available on the Mozilla Developer Network, and there are a number of [http://bradfrost.github.com/this-is-responsive/resources.html#viewport-testing tools for viewport testing].

=== Dimensions and units ===

==== A pixel is not a pixel ====

One of the major problems with using px (pixel) units on mobile devices is that a 'CSS pixel' (the unit used in a CSS rule) may not correspond to a 'device pixel' (the actual coloured dot on the display). This number of device pixels per unit of physical width is referred to as [http://en.wikipedia.org/wiki/List_of_displays_by_pixel_density pixel density]. (To determine the appropriate resolution for an image in a given context, the browser uses the device pixel ratio, as described in Boris Smus's [http://www.html5rocks.com/en/mobile/high-dpi/#toc-calculating-dpr article about high-DPI images] explains the meaning of device pixel ratio.)

[[File:device_pixel_ratio.png|thumb|400px|A diagram showing one reference angular pixel, to help illustrate how devicePixelRatio is calculated|alt=A diagram showing one reference angular pixel, to help illustrate how devicePixelRatio is calculated.]]

Browser vendors such as Apple and Mozilla found that sites displayed poorly on high-resolution devices (i.e. those with a high density of physical pixels) if browsers kept to a one-to-one ratio between CSS pixels and device pixels. As a result, this ratio varies across browsers and platforms.

This means that, unlike for print media, it is not advisable to attempt to specify absolute (physical) size for text, images or layout on the web. Peter Paul Koch has written a [http://www.quirksmode.org/blog/archives/2010/04/a_pixel_is_not.html very detailed guide] to this problem. Zoom compounds the situation: for more information, see [https://www.webkit.org/blog/55/high-dpi-web-sites/ High DPI sites] on the Surfin' Safari blog, and the Quirksmode post, [http://www.quirksmode.org/mobile/viewports.html A tale of two viewports].

As a result, one of the core techniques of responsive design is to use relative, not absolute units, and techniques for this are described throughout Koch's article.

== Media queries ==

CSS media queries allow you to choose different CSS rules for different browsing conditions, such as media (print or screen), display width or device orientation. Media queries are at the core of RWD approaches, because they enable web designers to specify different layouts and sizes for different contexts.

You can use media queries to apply different stylesheets:

 <nowiki>
<link rel='stylesheet' media='screen and (min-width: 400px) and (max-width: 800px)' href='css/smallish.css' />
</nowiki>

...or different rules:

 <nowiki>
@media all and (min-width: 300px) and (max-width: 600px) {
  header {
    background-image: url(bg_small.png);
    padding: 0.5em;
  }
}
</nowiki>

[http://mediaqueri.es/ mediaqueri.es] provides examples of sites that use media queries, Mozilla Developer Network provides [https://developer.mozilla.org/en-US/docs/CSS/Media_queries a detailed reference to media queries], and more details of features that may be implemented in the future are available from the [http://www.w3.org/TR/css3-mediaqueries/ W3C Recommendation].

==== Breakpoints ====

[[File:mediaqueri.es.png|thumb|left|400px|mediaqueri.es site|alt=mediaqueri.es site]]

'Breakpoint' is CSS-speak for the dimensions at which a different sets of style rules should be applied. Layout are liable to 'break' at particular sizes: for example, two 350px-wide images side by side with no padding or margin might overlap horizontally when the width of the viewport goes below 700px.

There are two ways to work out breakpoints:

* By device size, [http://www.html5rocks.com/en/mobile/cross-device/#toc-client-detect using common dimensions] for (say) phones, tablets, laptops and larger screens.
* Based on content, adding breakpoints at dimensions that make sense for your layouts.

The problem with the device-size approach is that the number of device types and sizes is continually changing, and boundaries are getting blurred. This makes it hard to maintain the 'right' device-oriented breakpoints. In general it may make more sense to add breakpoints to suit content, so layouts don't 'break' no matter what size the screen.

It's easy to test this out, with tools like Remy Sharp's [http://responsivepx.com/ responsivepx] and Brad Frost's [http://bradfrostweb.com/blog/post/ish/ ish].

==== Responsive design v Adaptive design v adaptive layout ====

[http://blog.easy-designs.net/archives/2011/11/16/on-adaptive-vs-responsive-web-design/ Adaptive web design] can respond to varying contexts without fluid grids and flexible images, for example by providing different page components in different contexts. Brad Frost [http://blog.easy-designs.net/archives/2011/11/16/on-adaptive-vs-responsive-web-design/ gives three examples] of design that is adaptive rather than responsive:

Can this device access my location? If so, inject a Use Current Location button onto the site in addition to the basic store-finder form.

Does this device understand touch events? If so, make this image carousel swipeable in addition to the previous and next buttons.

Does the browser support HTML5 canvas? If so, replace this static image with a canvas element.

For typography, images and layout, adaptive design might respond to breakpoints in a way that is not 'responsive': for example, by using fixed measures rather than fluid grids.

'Adaptive design' also refers more generally to the idea of [http://en.wikipedia.org/wiki/Progressive_enhancement progressive enhancement]: for example, providing location-based functionality for a web app on mobile devices, but not on the desktop.

The differences between 'adaptive' and 'responsive' have been summarised by [http://blog.easy-designs.net/archives/2011/11/16/on-adaptive-vs-responsive-web-design/ Aaron Gustafson], often credited with inventing the term 'adaptive design'. Marc ven den Dobbelsteen also used the term 'adaptive design' in his 2006 [http://www.alistapart.com/articles/switchymclayout Switch McLayout article]. Brad Frost [http://blog.easy-designs.net/archives/2011/11/16/on-adaptive-vs-responsive-web-design/ has suggested] that responsive design is a subset of adaptive design.

==== More information ====

Using media queries on mobile platforms: [http://mobile.smashingmagazine.com/2010/07/19/how-to-use-css3-media-queries-to-create-a-mobile-version-of-your-website/ http://mobile.smashingmagazine.com/2010/07/19/how-to-use-css3-media-queries-to-create-a-mobile-version-of-your-website/]

Reference: [https://developer.mozilla.org/en-US/docs/CSS/Media_queries developer.mozilla.org/en-US/docs/CSS/Media_queries]

W3C Recommendation: [http://www.w3.org/TR/css3-mediaqueries/ w3.org/TR/css3-mediaqueries]

== Testing ==

[[File:responsivepx.png|thumb|left|500px|Remy Sharp's responsivepx tool|alt=Remy Sharp's responsivepx tool]]

For responsive design to work well, it is especially important to test sites and applications at different viewport sizes.

Remy Sharp's [http://responsivepx.com/?simpl.info#640x480&scrollbars responsivepx] makes it possible to adjust viewport width and height values, in order to find the [https://docs.google.com/a/google.com/document/d/1wciRNw81BdIbuwzJJzcGJVhzkOvm1AZwS0KgULZAiZw/edit#heading=h.umsakrrk7jlc breakpoints] at which responsive layouts need to change. 

[[File:ish.png|thumb|500px|Brad Frost's ish resizer|alt=Brad Frost's ish resizer]]

Brad Frost's [http://bradfrostweb.com/demo/ish/ ish] resizer emphasises that breakpoints should be based on content rather than nominal device dimensions.


For responsive typography, [http://www.webtypography.net/Rhythm_and_Proportion/Horizontal_Motion/2.1.2/ designers have found] that body text should generally have between 45 and 75 characters per line. A simple trick for testing layouts [http://trentwalton.com/2012/06/19/fluid-type/ suggested by Trent Walton], is to add an asterisk to lorem text after 45 and 75 characters. If both asterisks appear on the same line at a particular viewport width, the font size needs to be changed.

A huge range of other tools is available for testing and debugging responsive design components including images, fonts and layouts. For more information and resources see the [http://docs.webplatform.org/wiki/concepts/internet_and_web/html5_hybrid_applications/concepts/mobile_debugging#Devices Mobile Debugging article] on webplatform.org.

== Pro and con ==

A word of warning: 'pure' RWD may not always be appropriate, and developers such as Guy Podjarny have pointed to [http://guypo.com/technical/responsive-web-design-is-bad-for-performance-there-i-said-it potential performance problems].

In [https://managewp.com/5-reasons-why-responsive-design-is-not-worth-it/comment-page-1 5 Reasons Why Responsive Design Is Not Worth It] Tom Ewer argues that RWD is simply a waste of time and money given that modern mobile browsers are designed to cope well with non-responsive sites (for example, by zooming elements to full width when they're tapped on). Ewer also suggests that providing different layouts for different browsing contexts is confusing to users.

Developers have encountered several other RWD hazards:

* Embedded components such as maps or games may not translate well to responsive designs
* Users may prefer the 'swipe and zoom' approach: getting a visual overview of a site, then zooming in to what interests them
* Providing different site layouts on different platforms might surprise users -- reducing trust, recognition and consistency -- even if site content is the same
* Website publishers need to monetize their sites and apps, and [http://www.netmagazine.com/features/state-responsive-advertising-publishers-perspective many ads are not responsive].
* Many developers have to work with existing code and content, and cannot not start from scratch. In this case [http://simplebits.com/notebook/2011/08/19/adapted/ hybrid approaches may be a better bet].
* Older browsers do not support media queries, CSS properties such as <tt>max-width</tt> and may not even support techniques such as relative sizing (or even have good support for fixed sizing). This can be a particular problem for the significant minority of browsers on low-end cellphones.

Some techniques for dealing with these issues are described below.

=== Coping with older browsers ===

==== Media queries ====

Scott Jehl's [https://github.com/scottjehl/Respond Respond.js polyfill] enables min-width and max-width rules, even with older browsers such as Internet Explorer 6 8; [http://www.jquery.com/ jQuery] likewise.

==== Feature detection ====

The [http://www.modernizr.com/ Modernizr] library works on most web platforms and can be used to build responsive sites and apps which work in a range of contexts.

==== Polyfills ====

A polyfill (think [http://www.wilkinsonplus.com/content/ebiz/wilkinsonplus/invt/0288365/0288365_l.jpg Polyfilla]) is code that enables features to be used natively, if they're available, or replicates them if they're not. This can be very useful for achieving future-proof RWD across a range of browsers.

=== High performance RWD ===

Several developers have suggested techniques to avoid or minimise performance problems with RWD.

Guy Podjarny: [http://guypo.com/technical/responsive-web-design-is-bad-for-performance-there-i-said-it Responsive Web Design Makes It Hard To Be Fast] and [http://www.slideshare.net/guypod/performance-implications-of-mobile-design-perf-audience-edition Performance Implications of Mobile Design]

Jason Grigsby: [http://lanyrd.com/2012/velocity/stpqq/ The Performance Implications of Responsive Web Design]

Brad Frost: list of RWD [http://bradfrost.github.com/this-is-responsive/resources.html#performance performance resources]

=== RWD opt out ===

[[File:bruce_lawson.png|thumb|left|300px|Bruce Lawson blog post: opting out of RWD|alt=Bruce Lawson blog post: opting out of RWD]]

Bruce Lawson and other developers have suggested that it might be appropriate to give users the option to opt out of RWD: his [http://www.brucelawson.co.uk/2013/turning-off-responsive-web-design/ blog post] on the subject, has links to articles explaining techniques for enabling this.

== Further reading ==

[http://www.alistapart.com/articles/responsive-web-design/ Responsive Web Design], by Ethan Marcotte

[http://bradfrost.github.com/this-is-responsive/ This is Responsive]: patterns, resources and news collated by Brad Frost

[http://www.alistapart.com/articles/dao/ The Dao of Web Design]: influential article by John Allsopp from April 2000: 'Now is the time for the medium of the web to outgrow its origins in the printed page.'

[http://www.alistapart.com/articles/ A List Apart articles on responsive design]

== Related concepts ==

Adaptive web design

[http://en.wikipedia.org/wiki/Progressive_enhancement Progressive enhancement]

[http://coding.smashingmagazine.com/2009/06/02/fixed-vs-fluid-vs-elastic-layout-whats-the-right-one-for-you/ Liquid layout]
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Grid Layout, Media Queries
}}
{{Topics|Design, Mobile, UI, Usability}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}