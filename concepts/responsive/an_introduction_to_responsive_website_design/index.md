---
title: an introduction to responsive website design
tags:
  - Concept
  - Pages
uri: 'concepts/responsive/an introduction to responsive website design'

---
 Responsive website design is an approach by which the website adjusts itself dynamically to give the best user experience for the particular device. For example pages viewed in a desktop can have links that are text based and compact, but for touch screen devices the links should be big enough for touch based interactions. Responsive web design aims to tackle these differences using certain techniques that are available in HTML5 and CSS3 without the need to serve different pages for different devices.

The major techniques used are

-   CSS3 media queries that help the CSS to change depending on device specifications like pixel density, screen resolution, orientation etc.
-   Use relative scales instead of fixed scales. Specify widths in percentage and font size in em/rem so that the page adapts to the device screen without the need of panning or zooming out.

The problem is that at present the support for HTML5 techniques varies widely with different browsers and different mobile device screen resolutions further complicate design - what looks fine on a mobile may waste space on a tablet.

The technical compatibility issues are a serious problem but libraries such as <http://html5boilerplate.com/> make this much simpler, allowing you to focus on writing 'pure' HTML5 while it juggles with the contortions required for each type of browser.

A responsive layout needs thought at the design level, so page content reflows and adjusts to suit. But you also need to remember that what looks slick on a desktop site (a large crossfading background and nice popup dialogs) can kill usability on a mobile device. I have seen sites with modal popups (i.e. they lock the whole screen until you close them) that open automatically, for example 'Do you want to complete a survey?'. The problem is that on a mobile or even a small tablet the dialog close button isn't visible, and you have to scroll around the screen until you find it. This is the definition of *un*responsive design.
