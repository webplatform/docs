{{Page_Title|SVG introduction}}
{{Flags}}
{{Byline}}
{{Summary_Section|This page provides some background on SVG: what it is, and how it is useful.}}
{{Guide
|Content=[[Image:=SVG_Overview.png|=SVG_Overview.png]][[SVG]] is an [[XML]] language, similar to [[XHTML]], which can be used to draw graphics, such as the ones shown to the right. It can be used to create an image either by specifying all the lines and shapes necessary, by modifying already existing raster images, or by a combination of both. The image and its components can also be transformed, composited together, or filtered to change its appearance completely.
 
SVG came about in 1999 after several competing formats had been submitted to the [[W3C]] and failed to be fully ratified. While the specification has been around for quite awhile, browser adoption has been fairly slow, and so there is not a lot of SVG content being used on the web right now (2009). Even the implementations that are available often are not as fast as competing technologies like [[HTML:Canvas]] or Adobe Flash as a full application interface. SVG does offer benefits over both implementations some of which include having a DOM interface available for it, and not requiring 3rd party extensions to the default browser to work. Whether to use it or not often depends on what you are using it for.
 
=== Basic ingredients ===
 
HTML provides elements for defining headers, paragraphs, tables and so on. In much the same way SVG provides elements for circles, rectangles, and simple and complex curves. A simple SVG document consists of nothing more than the <code>svg</code> root element and several basic shapes that build a graphic together. In addition there is the <code>g</code> element, which is used to group several basic shapes together.

Starting from there, the SVG image can become arbitrarily complex. SVG supports gradients, rotations, filter effects, animations, interaction with JavaScript, and so on. But all these extra features of the language rely on this relatively small set of elements to define the graphic area.
 
=== Before you start ===
 
There are a number of drawing applications available such as [[Inkscape]] which are free and use SVG as their native file format. However, this tutorial will rely on the trusty XML or text editor (your choice). The idea is to teach the internals of SVG to those who want to understand it, and that is best done by dirtying your hands with a bit of markup. You should note your final goal though. Not all SVG viewers are equal and so there is a good chance that something written for one app will not display exactly the same in another, simply because they support different levels of the SVG specification or another specification that you are using along with SVG (that is [[JavaScript]] or [[CSS]]).
 
SVG is not supported in all modern browsers (although its getting there). A fairly complete list of SVG viewers is given on the [[SVG Wiki]]. Firefox has supported some SVG content since version 1.5, and that support level has been growing with each release since. Hopefully, along with the tutorial here, MDC can help developers keep up with the differences between Gecko and some of the other major implementations.
 
Before starting you should have a basic understanding of XML or another markup language such as HTML. If you are not too familiar with XML, here are some guidelines to keep in mind:
 
* SVG elements and attributes should all be entered in the case shown here since XML is case-sensitive (unlike HTML).
* Attribute values in SVG must be placed inside quotes, even if they are numbers.
 
SVG is a huge specification. This tutorial attempts to cover the basics. Once you are familiar you should be able to use the [[Element Reference]] and the [[Interface Reference]] to find out anything else you need to know.

=== Flavors of SVG ===
 
Since becoming a recommendation in 2003, the most recent "full" SVG version is 1.1. It builds on top of SVG 1.0, but adds more modularization to ease implementation. A second edition of SVG 1.1 is being worked on at the moment. "Full" SVG 1.2 was meant to be the next major release of SVG. It was dropped for the upcoming SVG 2.0, which is under heavy development right now and follows a similar approach to CSS 3 in that it splits components in several loosely coupled specifications.

Apart from the full SVG recommendations, the working group at the W3C introduced SVG Tiny and SVG Basic in 2003. These two profiles are aimed mainly at mobile devices. The first, SVG Tiny, should yield graphic primitives for small devices with low capabilities. SVG Basic offers many features of full SVG, but doesn't include the ones which are hard to implement or heavy to render (like animations). In 2008 SVG Tiny 1.2 became a W3C Recommendation.
 
There were plans for an SVG Print specification, which would add support for multiple pages and enhanced color management. This work was discontinued.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Introduction
|MSDN_link=
|HTML5Rocks_link=
}}