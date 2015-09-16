---
title: 'Mobile web debugging'
readiness: 'Ready to Use'
summary: 'Debugging web applications on multiple platforms requires careful prioritisation, different from developing for desktop alone. This article explains techniques and tools available, with links to external resources.'
tags:
  - Concept
  - Pages
  - Developer
  - Tools
  - Mobile
  - Design
  - Performance
uri: 'concepts/mobile web/mobile debugging'

---
## Summary

Debugging web applications on multiple platforms requires careful prioritisation, different from developing for desktop alone. This article explains techniques and tools available, with links to external resources.

# Mobile web debugging

## Summary

<span data-meta="summary" data-type="key"><span data-type="value">Debugging web applications on multiple platforms requires careful prioritisation. This article explains techniques and tools available, with links to external resources.</span></span>

## Quick start

1.  Prioritise testing on a variety of [real devices](#Devices).
2.  Add [simulators and emulators](#Simulators_and_emulators) to your toolkit.
3.  Use [remote debugging tools](#Remote_debugging) such as [Chrome DevTools](#Chrome_DevTools) and [Adobe Edge Inspect](#Adobe_Edge_Inspect).
4.  [Report bugs](#Reporting_browser_bugs)!

## Understanding hardware

Debugging for mobile can be more complex and demanding than for desktop, simply because mobile devices often have a complex variety of functions and inputs:

-   Telephone
-   Camera
-   GPS
-   Accelerometer
-   Gyroscope
-   Proximity detector
-   Ambient light sensor
-   Multi-touch, gestures and keyboards

CPU, memory and storage are far more constrained and variable on mobile devices than for desktops and laptops, and debugging needs to be done with the whole mobile stack in mind:

-   network
-   hardware
-   browser software
-   app software

## Context

Two factors are characteristic of mobile web usage: variability and instability. Both can lead to a buggy user experience.

Variability:

-   Devices: screen size and resolution, touch screen type and quality, CPU, memory, storage – even for devices running the same OS
-   Users: they're mobile – changing location, context and mood
-   Latency: there is a massive range of potential delays at every 'hop'
-   Bandwidth: far less predictable than desktop
-   Location: position in a network cell, distance from wifi access points
-   Time of day: mobile users are likely to access web apps at all times of day and night – bandwidth and latency vary considerably at different times
-   Carrier: different carriers may provide different levels of bandwidth and latency

Instability:

-   Flakey cell connectivity
-   On/off: train through a tunnel, moving between network cells or rooms
-   Poor and shared wifi
-   Cheap, low-spec devices: slower CPU, less memory, lower quality displays and less responsive touch screens
-   More failed UI interactions than for desktop devices

When dealing with bugs, it's also important to consider user context: environment, mood, posture and time of day. Different contexts have different performance requirements: watching video while lying on a sofa compared to quickly checking a map while on a crowded bus, for example. The variety of usage contexts on mobile is likely to expose more bugs than for a traditional desktop setup in which a person sits at a table using a keyboard and mouse, with a large display and a computer 'plumbed in' for power and network connectivity.

To get a sense of what people are actually consuming on the mobile web, take a look at [HTTP Archive Mobile](http://mobile.httparchive.org). This provides analysis of browsing data for Alexa's top one million sites.

## Devices

Facebook data show that [over 7000 different devices access their site every day](http://techcrunch.com/2012/08/03/vp-mike-schroepfer-7000-different-mobile-devices-access-facebook-every-day/). Even if your site or app doesn't have this level of traffic, it's important to test web apps on multiple platforms, and to develop a strategy for prioritising which devices and browsers to test on.

If you don't have access to many devices, there may be an open device lab near you, where you can use or even borrow devices for free: [www.opendevicelab.com](http://www.opendevicelab.com).

More suggestions on how to set up a device lab:
[dmolsen.com/mobile-in-higher-ed/2012/06/26/how-to-build-a-device-lab-part-1](http://www.dmolsen.com/mobile-in-higher-ed/2012/06/26/how-to-build-a-device-lab-part-1/)

Strategies for choosing devices:
[stephanierieger.com/strategies-for-choosing-test-devices](http://stephanierieger.com/strategies-for-choosing-test-devices/)

Testing 'without breaking the bank':
[bradfrostweb.com/blog/mobile/test-on-real-mobile-devices-without-breaking-the-bank](http://bradfrostweb.com/blog/mobile/test-on-real-mobile-devices-without-breaking-the-bank/)

## Mobile simulation in the browser

Before testing on mobile devices, it's often best to do as much design and development as possible on a development computer. With that in mind, a number of tools have been built to mimic the mobile environment in the browser.

### Chrome DevTools

Chrome provides many features for mobile device simulation:
 - touch simulation
 - user agent overriding
 - device metrics overriding (resolution and font scale factor)

### Firefox

Firefox provides Responsive Design View:
[developer.mozilla.org/en-US/docs/Tools/Responsive\_Design\_View](https://developer.mozilla.org/en-US/docs/Tools/Responsive_Design_View)

Other Firefox developer tools are listed here:
[developer.mozilla.org/en-US/docs/Tools](https://developer.mozilla.org/en-US/docs/Tools)

### Debugging responsive design

[Responsive Web Design](http://www.alistapart.com/articles/responsive-web-design/) (RWD for short) is an approach that emphasises design which works well across a variety of platforms, in particular by using [media queries](http://www.html5rocks.com/en/mobile/responsivedesign/?redirect_from_locale=ja#toc-style-mediaqueries), [fluid grids](http://www.alistapart.com/articles/fluidgrids/) (layouts) and [fluid images](http://www.alistapart.com/articles/fluid-images/).

For responsive design to work well, it is especially important to test sites and applications at different viewport sizes. Remy Sharp's [responsivepx](http://responsivepx.com/?simpl.info#640x480&scrollbars) makes it possible to adjust viewport width and height values, in order to find points at which responsive layouts 'break'. Developer Brad Frost recently produced the [ish resizer](http://bradfrostweb.com/demo/ish/), which emphasises that 'breakpoints' – size ranges for displaying particular layouts and content – should be based on content rather than fixed device dimensions.

For responsive typography, [designers have found](http://www.webtypography.net/Rhythm_and_Proportion/Horizontal_Motion/2.1.2/) that body text should generally have between 45 and 75 characters per line, A very simple trick for testing layouts, [suggested by Trent Walton](http://trentwalton.com/2012/06/19/fluid-type/), is to add an asterisk to \_lorem\_ text after 45 and 75 characters. If both asterisks appear on the same line at a particular viewport width, the font size needs to be changed.

A [huge range of other tools](http://bradfrost.github.com/this-is-responsive/resources.html#viewport-testing) is available for testing and debugging responsive design components including images, fonts and layouts.

## Simulators and emulators

Simulators aim only to mimic the behaviour of a device. Emulators are designed to replicate the way a device actually works, in terms of hardware and software. For example, the Android emulator runs a full Android system stack down to the kernel level, whereas iOS provides a simulator. (There's a [long discussion on Stack Overflow](http://stackoverflow.com/questions/1584617/simulator-or-emulator-what-is-the-difference) on the difference.)

Simulators and emulators are available for many platforms, and browsers can be installed on most of these: [mobilexweb.com/emulators](http://www.mobilexweb.com/emulators). (It's not included on this list, but a simulator is also available for the [Kindle Fire](https://developer.amazon.com/sdk/fire/emulator-guide.html).)

-   [Android emulator](http://developer.android.com/tools/devices/emulator.html)
-   [iOS simulator](http://developer.apple.com/library/ios/#DOCUMENTATION/Xcode/Conceptual/ios_development_workflow/25-Using_iOS_Simulator/ios_simulator_application.html)

The [Opera Mobile simulator](http://www.opera.com/developer/tools/mobile/) can run multiple Opera Mobile instances, each with its own settings (such as resolution and pixel density) and can be used in collaboration with the Opera Dragonfly development tools.

### Online tools

Several paid-for online tools enable developers to test sites in a variety of real or virtual devices and browsers.

[Appthwack](https://appthwack.com) gives screenshots from different browsers running on real devices, and provides load time estimates.

[BrowserStack](https://browserstack.com) allows interaction with emulators or simulators running on virtual machines.

[Perfecto Mobile](http://www.perfectomobile.com/portal/cms/services/web_access_to_real_handsets.html) and [DeviceAnywhere](http://www.keynotedeviceanywhere.com/da-free-product-overview.html) also use real devices.

[Saucelabs](https://saucelabs.com/) provides integration with Selenium RC and WebDriver.

## Remote debugging

Several tools enable developers to run a debugger user interface on one device in order to debug a web page running on another: for example, from your laptop debug a web page displayed on your phone.

Most tools for remote debugging require some setup; in particular, browser tools require port forwarding to be initiated from the command line.

### Chrome DevTools

The Chrome tools enable remote debugging via USB. The full set of developer tools is available, including:

-   Console
-   JavaScript debugger
-   DOM access
-   DOM debugger
-   Network and resource tools
-   Source information and editing
-   Timeline data

For more information see [developers.google.com/chrome-developer-tools/docs/remote-debugging](https://developers.google.com/chrome-developer-tools/docs/remote-debugging).

### WebKit remote debugging

The WebKit Web Inspector is implemented as an HTML + CSS + JavaScript web application that can run outside of the browser environment, and has been incorporated in other debugging tools. Chrome DevTools developer Pavel Feldman's [article about remote debugging](http://www.google.com/url?q=http%3A%2F%2Fwebkit.org%2Fblog%2F1620%2Fwebkit-remote-debugging&sa=D&sntz=1&usg=AFQjCNGF6wUdoJzskoR5CBEY8AlWz6I3Zw) provides a quick tutorial (albeit oriented to desktop Chromium) and discusses the Remote Debugging Protocol. Safari's Web inspector uses the WebKit remote debugging protocol.

[Safari on Mac OS X can be used for remote debugging](http://developer.apple.com/library/ios/#documentation/AppleApplications/Reference/SafariWebContent/DebuggingSafarioniPhoneContent/DebuggingSafarioniPhoneContent.html) of HTML, CSS and JavaScript running in Safari on iOS 6 (or later) or on a simulator. There's a short screencast at [screenr.com/GYZ8](http://www.screenr.com/GYZ8).

More information about web app debugging on iOS is available from [mobilexweb.com/blog/iphone-5-ios-6-html5-developers](http://www.mobilexweb.com/blog/iphone-5-ios-6-html5-developers).

General information about using the iOS simulator is available from [Apple's Xcode documentation](http://developer.apple.com/library/ios/#documentation/Xcode/Conceptual/ios_development_workflow/00-About_the_iOS_Application_Development_Workflow/introduction.html).

Information about BlackBerry debugging is available from the [HTML5 WebWorks](https://developer.blackberry.com/html5/documentation/enabling_webinsp_microsite_1987478_11.html) site, and RIM's Playbook OS also [supports Web Inpector](http://devblog.blackberry.com/2012/02/web-inspector-playbook/).

### weinre

Remote debugging tool. Reuses WebKit Web Inspector – and is used by Adobe Edge Inspect.

Useful for remote debugging with pre-Jelly Bean (4.1) Android devices, and iOS pre version 5:
[people.apache.org/\~pmuellr/weinre/docs/latest](http://people.apache.org/~pmuellr/weinre/docs/latest/).

### Adobe Edge Inspect

Previously known as Adobe Shadow; uses weinre (see above) for remote inspection.

[FAQs](http://www.google.com/url?q=http%3A%2F%2Fhtml.adobe.com%2Fedge%2Finspect%2Ffaq.html&sa=D&sntz=1&usg=AFQjCNGcywotr4i2S-ZTb_Cij61JacHMJQ)

[Setup and usage instructions](http://www.adobe.com/devnet/edge-inspect/articles/browser-testing-across-devices-with-adobe-edge-inspect.html)

Edge Inspect enables wireless synchronised browsing on multiple devices, as well as remote inspection, screenshot tools and other features. A number of platforms are supported. Edge Inspect is available as part of Adobe's Creative Cloud for free and paid memberships.

Installation requires three steps:
 1. Install Edge Inspect on the development computer.
 2. Install Chrome and the Edge Inspect Chrome Extension on development computer.
 3. Install the Edge Inspect application on iOS and/or Android devices.

Adobe has also published a [beginner's guide](http://blogs.adobe.com/mallika/2012/10/beginners-guide-to-adobe-edge-tools-services.html) to the Edge tools.

### Firefox remote debugging

Firefox has tools for remote debugging, though these are currently more limited than the Chrome tools:
 - remote debugging only for scripts, i.e. not HTML or CSS or anything else
 - after opening the remote debugging window, incoming requests must be accepted on the secondary device
 - breakpoints can be set, and there is a scope panel, but no console, so you can't get variable values (or information about an object by hovering over it, as with the Chrome tools)

The Firefox tools can be used via wifi. Note, however, that debugging via wifi affects the remote device's connectivity environment, unlike connecting via USB.

Instructions from the Mozilla blog:
[hacks.mozilla.org/2012/08/remote-debugging-on-firefox-for-android](https://hacks.mozilla.org/2012/08/remote-debugging-on-firefox-for-android/)

Screencast:
[youtube.com/watch?v=Znj\_8IFeTVs](http://www.youtube.com/watch?v=Znj_8IFeTVs)

Information about the Mozilla remote debugging protocol:
[wiki.mozilla.org/Remote\_Debugging\_Protocol](https://wiki.mozilla.org/Remote_Debugging_Protocol)

### Firebug

There is a bookmarklet that allows Firebug to run on iOS:
[martinkool.com/post/13629963755/firebug-on-ipad-and-iphone](http://martinkool.com/post/13629963755/firebug-on-ipad-and-iphone)

### iWebInspector

This tool, built by Maximiliano Firtman, can be useful for debugging apps running on Safari for iOS pre version 6.0 – can also be used with PhoneGap apps: [iwebinspector.com](http://www.iwebinspector.com/).

## Debugging performance issues

Performance bugs are a significant barrier to producing a successful site or web app.

For more information about improving mobile web performance, see Google's [mobile web best practice documentation](https://developers.google.com/speed/docs/best-practices/mobile).

### Memory

When considering performance problems, bear in mind that some bugs go unnoticed on desktop computers but become problematic on devices with more constrained memory and caching. Remember that users – even on mobile – are leaving web apps [open for longer than they used to](http://www.samdutton.com/devoxx2012/#76). In particular, beware of memory leaks when using event listeners or creating DOM elements.

The Chrome DevTools have [several features for analysing memory usage](https://developers.google.com/chrome-developer-tools/docs/memory-analysis-101). These tools also provide a timeline and Frame Mode for understanding the time taken to display each 'frame' in the browser – loading, scripting, rendering and painting – and how to maintain an acceptable 'frame rate'.

### window.performance

The Navigation Timing API is a great 'tool' for debugging performance problems:
[html5rocks.com/en/tutorials/webperformance/basics](http://www.html5rocks.com/en/tutorials/webperformance/basics/).

The API provides timing data for page load and navigation events, including DNS resolution and redirects. Data from the web.performance [can be accessed via Google Analytics](http://analytics.blogspot.nl/2012/04/more-ways-to-measure-your-websites.html).

### Performance checking

In order to avoid performance bugs, it is crucial to incorporate performance checking in your workflow.

There are several tools for this.

**Page Speed**
[developers.google.com/speed/pagespeed](https://developers.google.com/speed/pagespeed)
 Google tool to 'help developers optimize their web pages by applying web performance best practices'. A similar tool is available from the Audit panel in the Chrome DevTools.

**Blaze**
[akamai.com/blaze](http://www.akamai.com/blaze)
 Akamai service for 'front end optimisation'.

W3C also offers a tool to check web pages for 'mobile friendliness': [validator.w3.org/mobile](http://validator.w3.org/mobile/).

## Browser and device capability

It's important to ensure that your target platforms support the HTML, JavaScript and CSS features you use, and to plan sensible fallback strategies. Several sites provide detailed, up-to-date information about this.

[caniuse.com](http://www.caniuse.com)
 Mobile and desktop browser capabilities, with links to documentation

[mobilehtml5.org](http://mobilehtml5.org)
 Capability information for mobile browsers.

[modernizr.com](http://www.modernizr.com)
 Feature detection library supported by most web platforms.

[html5please.us](http://www.html5please.us)
 HTML, CSS and JavaScript features: what's in flux, what's flakey, and what you can do about it.

[html5test.com](http://html5test.com)
[haz.io](http://haz.io)
 Check HTML, CSS and JavaScript features supported by your browser.

[css3test.com](http://www.css3test.com)
 Test for CSS3 feature support.

[jsperf.com](http://www.jsperf.com)
 An easy way to create, run, compare and share JavaScript test cases.

[overlooksoft.com/fing](http://www.overlooksoft.com/fing)
 Fing is a native app for checking the network environment – you can even run ping and traceroute.

## Reporting browser bugs

It's extremely important for the developer community that you report browser bugs as soon as you encounter them, however frustrating or trivial they may seem.

For more information about how to report bugs – and why you should do that – see [coding.smashingmagazine.com/2011/09/07/help-the-community-report-browser-bugs](http://coding.smashingmagazine.com/2011/09/07/help-the-community-report-browser-bugs/).

Simple bug reporting tool for Chrome for Android: [new.mcrbug.com](http://new.mcrbug.com)

Safari: [developer.apple.com/bugreporter](https://developer.apple.com/bugreporter/)

Opera: [bugs.opera.com/wizard](https://bugs.opera.com/wizard/)

Firefox: [bugzilla.mozilla.org](https://bugzilla.mozilla.org/)

Internet Explorer: [connect.microsoft.com](http://connect.microsoft.com/)

## And finally...

Whatever you build, try to test it on a variety of mobile devices in a variety of contexts.

You don't need a complex test suite and usability lab for that: just get friends and colleagues to try out what you've built. [Discount usability](http://www.useit.com/alertbox/discount-usability.html) is a lot better than none at all!

The mobile web is changing fast, unpredictably – what matters now may not matter in six months – so make sure to incorporate testing early in your workflow.

## Learn more

Brad Frost's guide to testing and tools:
[mobilewebbestpractices.com/resources/\#r-testing](http://mobilewebbestpractices.com/resources/#r-testing)

Smashing Magazine articles about mobile web app design:
[mobile.smashingmagazine.com](http://mobile.smashingmagazine.com/)

HTML5 Rocks articles about mobile web development:
[html5rocks.com/](http://www.html5rocks.com/en/mobile)[mobile](http://www.html5rocks.com/en/mobile)

Optimising mobile web app performance:
[developers.google.com/speed/docs/best-practices/mobile](https://developers.google.com/speed/docs/best-practices/mobile)

Ilya Grigorik on performance:
[igvita.com/slides/2012/webperf-crash-course.pdf](http://www.igvita.com/slides/2012/webperf-crash-course.pdf)

Brian Leroux on debugging mobile web apps:
[brian.io/slides/debug-mobile](http://brian.io/slides/debug-mobile/#/)

Resources for finding information about web development, and how to help others:
[movethewebforward.org](http://movethewebforward.org/)
