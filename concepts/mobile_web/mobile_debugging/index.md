{{Page_Title|Mobile debugging}}
{{Flags}}
{{API_Name}}
{{Summary_Section|Debugging web applications on multiple platforms requires careful prioritisation, different from developing for desktop alone. This article explains techniques and tools available, with links to external resources.}}
{{Concept_Page
|Content=== Quick start ==

# Prioritise testing on a variety of [[#Devices|real devices]].
# Add  [[#Simulators and emulators|simulators and emulators]] to your toolkit.
# Use [[#Remote debugging|remote debugging tools]] such as [[#Chrome DevTools|Chrome DevTools]] and [[#Adobe Edge Inspect|Adobe Edge Inspect]].
# [[#Reporting browser bugs|Report bugs]]!

== Understanding hardware ==

Debugging for mobile can be more complex and demanding than for desktop, simply because mobile devices often have a complex variety of inputs:

* Telephone
* Camera
* GPS
* Accelerometer
* Gyroscope
* Proximity detector
* Ambient light sensor
* Multi-touch, gestures and keyboards

CPU, memory and storage are far more constrained and variable on mobile devices than for desktops and laptops, and debugging needs to be done with the whole mobile stack in mind:

* network
* hardware
* browser software
* app software

== Context ==

Two factors are characteristic of mobile web usage: variability and instability. Both can lead to a buggy user experience.

Variability:

* Devices: screen size and resolution, touch screen type and quality, CPU, memory, storage &ndash; even for devices running the same OS
* Users: they're mobile &ndash; changing location, context and mood
* Latency: there is a massive range of potential delays at every 'hop'
* Bandwidth: far less predictable than desktop
* Location: position in a network cell, distance from wifi access points
* Time of day: mobile users are likely to access web apps at all times of day and night – bandwidth and latency vary considerably at different times
* Carrier: different carriers may provide different levels of bandwidth and latency

Instability:

* Flakey cell connectivity
* On/off: train through a tunnel, moving between network cells or rooms
* Poor and shared wifi
* Cheap, low-spec devices: slower CPU, less memory, lower quality displays and less responsive touch screens
* More failed UI interactions than for desktop devices

When dealing with bugs, it's also important to consider user context: environment, mood, posture and time of day. Different contexts have different performance requirements: watching video while lying on a sofa compared to quickly checking a map while on a crowded bus, for example. The variety of usage contexts on mobile is likely to expose more bugs than for a traditional desktop setup in which a person sits at a table using a keyboard and mouse, with a large display and a computer 'plumbed in' for power and network connectivity.

To get a sense of what people are actually consuming on the mobile web, take a look at [http://mobile.httparchive.org HTTP Archive Mobile]. This provides analysis of browsing data for Alexa's top one million sites.

== Devices ==

Facebook data show that [http://techcrunch.com/2012/08/03/vp-mike-schroepfer-7000-different-mobile-devices-access-facebook-every-day/ over 7000 different devices access their site every day]. Even if your site or app doesn't have this level of traffic, it's important to test web apps on multiple platforms, and to develop a strategy for prioritising which devices and browsers to test on.

If you don't have access to many devices, there may be an open device lab near you, where you can use or even borrow devices for free: [http://mobile.smashingmagazine.com/2012/09/24/establishing-an-open-device-lab/ mobile.smashingmagazine.com/2012/09/24/establishing-an-open-device-lab].

More suggestions on how to set up a device lab:<br/> [http://www.dmolsen.com/mobile-in-higher-ed/2012/06/26/how-to-build-a-device-lab-part-1/ dmolsen.com/mobile-in-higher-ed/2012/06/26/how-to-build-a-device-lab-part-1]

Strategies for choosing devices: <br/> [http://stephanierieger.com/strategies-for-choosing-test-devices/ stephanierieger.com/strategies-for-choosing-test-devices]

Testing 'without breaking the bank': <br/> [http://bradfrostweb.com/blog/mobile/test-on-real-mobile-devices-without-breaking-the-bank/ bradfrostweb.com/blog/mobile/test-on-real-mobile-devices-without-breaking-the-bank]

== Mobile simulation in the browser ==

Before testing on mobile devices, it's often best to do as much design and development as possible on a development computer. With that in mind, a number of tools have been built to mimic the mobile environment in the browser.

=== Chrome DevTools ===

Chrome provides many features for mobile device simulation:<br/>
- touch simulation<br/>
- user agent overriding<br/>
- device metrics overriding (resolution and font scale factor)

=== Firefox ===

Firefox provides Responsive Design View:<br/> [https://developer.mozilla.org/en-US/docs/Tools/Responsive_Design_View developer.mozilla.org/en-US/docs/Tools/Responsive_Design_View]

Other Firefox developer tools are listed here: <br/> [https://developer.mozilla.org/en-US/docs/Tools developer.mozilla.org/en-US/docs/Tools]

=== Viewport testing apps ===

A huge range of tools is available to try out different viewport sizes:<br/> [http://bradfrost.github.com/this-is-responsive/resources.html#viewport-testing bradfrost.github.com/this-is-responsive/resources.html#viewport-testing]

Developer Brad Frost recently produced the [http://bradfrostweb.com/demo/ish/ ish resizer]. This tool emphasises that 'breakpoints' &ndash; size ranges for displaying particular layouts and content &ndash; should be based on content rather than fixed device dimensions.

== Simulators and emulators ==

Simulators aim only to mimic the behaviour of a device. Emulators are designed to replicate the way a device actually works, in terms of hardware and software. For example, the Android emulator runs a full Android system stack down to the kernel level, whereas iOS provides a simulator. (There's a [http://stackoverflow.com/questions/1584617/simulator-or-emulator-what-is-the-difference long discussion on Stack Overflow] on the difference.)

Simulators and emulators are available for many platforms, and browsers can be installed on most of these: [http://www.mobilexweb.com/emulators mobilexweb.com/emulators]. (It's not included on this list, but a simulator is also available for the [https://developer.amazon.com/sdk/fire/emulator-guide.html Kindle Fire].)

* [http://developer.android.com/tools/devices/emulator.html Android emulator]
* [http://developer.apple.com/library/ios/#DOCUMENTATION/Xcode/Conceptual/ios_development_workflow/25-Using_iOS_Simulator/ios_simulator_application.html iOS simulator]

The [http://www.opera.com/developer/tools/mobile/ Opera Mobile simulator] can run multiple Opera Mobile instances, each with its own settings (such as resolution and pixel density) and can be used in collaboration with the Opera Dragonfly development tools.

== Remote debugging ==

Several tools enable developers to run a debugger user interface on one device in order to debug a web page running on another: for example, from your laptop debug a web page displayed on your phone.

Most tools for remote debugging require some setup; in particular, browser tools require port forwarding to be initiated from the command line.

=== Chrome DevTools ===

The Chrome tools enable remote debugging via USB. The full set of developer tools is available, including:

* Console
* JavaScript debugger
* DOM access
* DOM debugger
* Network and resource tools
* Source information and editing
* Timeline data

For more information see [https://developers.google.com/chrome-developer-tools/docs/remote-debugging developers.google.com/chrome-developer-tools/docs/remote-debugging].

=== WebKit remote debugging ===

The WebKit Web Inspector is implemented as an HTML + CSS + JavaScript web application that can run outside of the browser environment, and has been incorporated in other debugging tools. Chrome DevTools developer Pavel Feldman's [http://www.google.com/url?q=http%3A%2F%2Fwebkit.org%2Fblog%2F1620%2Fwebkit-remote-debugging&sa=D&sntz=1&usg=AFQjCNGF6wUdoJzskoR5CBEY8AlWz6I3Zw article about remote debugging] provides a quick tutorial (albeit oriented to desktop Chromium) and discusses the Remote Debugging Protocol. Safari's Web inspector uses the WebKit remote debugging protocol.

[http://developer.apple.com/library/ios/#documentation/AppleApplications/Reference/SafariWebContent/DebuggingSafarioniPhoneContent/DebuggingSafarioniPhoneContent.html Safari on Mac OS X can be used for remote debugging] of HTML, CSS and JavaScript running in Safari on iOS 6 (or later) or on a simulator. There's a short screencast at [http://www.screenr.com/GYZ8 screenr.com/GYZ8].

More information about web app debugging on iOS is available from [http://www.mobilexweb.com/blog/iphone-5-ios-6-html5-developers mobilexweb.com/blog/iphone-5-ios-6-html5-developers].

General information about using the iOS simulator is available from [http://developer.apple.com/library/ios/#documentation/Xcode/Conceptual/ios_development_workflow/00-About_the_iOS_Application_Development_Workflow/introduction.html Apple's Xcode documentation].

=== weinre ===

Remote debugging tool. Reuses WebKit Web Inspector &ndash; and is used by Adobe Edge Inspect.

Useful for remote debugging with pre-Jelly Bean (4.1) Android devices, and iOS pre version&nbsp;5: <br/> [http://people.apache.org/~pmuellr/weinre/docs/latest/ people.apache.org/~pmuellr/weinre/docs/latest].

=== Adobe Edge Inspect ===

Previously known as Adobe Shadow; uses weinre (see above) for remote inspection.

[http://www.google.com/url?q=http%3A%2F%2Fhtml.adobe.com%2Fedge%2Finspect%2Ffaq.html&sa=D&sntz=1&usg=AFQjCNGcywotr4i2S-ZTb_Cij61JacHMJQ FAQs]

[http://www.adobe.com/devnet/edge-inspect/articles/browser-testing-across-devices-with-adobe-edge-inspect.html Setup and usage instructions]

Edge Inspect enables wireless synchronised browsing on multiple devices, as well as remote inspection, screenshot tools and other features. A number of platforms are supported. Edge Inspect is available as part of Adobe's Creative Cloud for free and paid memberships.

Installation requires three steps:<br/> 1. Install Edge Inspect on the development computer.<br/> 2. Install Chrome and the Edge Inspect Chrome Extension on development computer.<br/> 3. Install the Edge Inspect application on iOS and/or Android devices.

Adobe has also published a [http://blogs.adobe.com/mallika/2012/10/beginners-guide-to-adobe-edge-tools-services.html beginner's guide] to the Edge tools.

=== Firefox remote debugging ===

Firefox has tools for remote debugging, though these are currently more limited than the Chrome tools:<br/> - remote debugging only for scripts, i.e. not HTML or CSS or anything else<br/> - after opening the remote debugging window, incoming requests must be accepted on the secondary device<br/> - breakpoints can be set, and there is a scope panel, but no console, so you can't get variable values (or information about an object by hovering over it, as with the Chrome tools)

The Firefox tools can be used via wifi. Note, however, that debugging via wifi affects the remote device's connectivity environment, unlike connecting via USB.

Instructions from the Mozilla blog:<br/> [https://hacks.mozilla.org/2012/08/remote-debugging-on-firefox-for-android/ hacks.mozilla.org/2012/08/remote-debugging-on-firefox-for-android]

Screencast:<br/> [http://www.youtube.com/watch?v=Znj_8IFeTVs youtube.com/watch?v=Znj_8IFeTVs]

Information about the Mozilla remote debugging protocol:<br/> [https://wiki.mozilla.org/Remote_Debugging_Protocol wiki.mozilla.org/Remote_Debugging_Protocol]

=== Firebug ===

There is a bookmarklet that allows Firebug to run on iOS:<br/> [http://martinkool.com/post/13629963755/firebug-on-ipad-and-iphone martinkool.com/post/13629963755/firebug-on-ipad-and-iphone]

=== iWebInspector ===

This tool, built by Maximiliano Firtman, can be useful for debugging apps running on Safari for iOS pre version 6.0 – can also be used with PhoneGap apps: [http://www.iwebinspector.com/ iwebinspector.com].

== Debugging performance issues ==

Performance bugs are a significant barrier to producing a successful site or web app.

For more information about improving mobile web performance, see Google's [https://developers.google.com/speed/docs/best-practices/mobile mobile web best practice documentation].

=== Memory ===

When considering performance problems, bear in mind that some bugs go unnoticed on desktop computers but become problematic on devices with more constrained memory and caching. Remember that users &ndash; even on mobile &ndash; are leaving web apps [http://www.samdutton.com/devoxx2012/#76 open for longer than they used to]. In particular, beware of memory leaks when using event listeners or creating DOM elements.

The Chrome DevTools have [https://developers.google.com/chrome-developer-tools/docs/memory-analysis-101 several features for analysing memory usage]. These tools also provide a timeline and Frame Mode for understanding the time taken to display each 'frame' in the browser – loading, scripting, rendering and painting – and how to maintain an acceptable 'frame rate'.

=== window.performance ===

The Navigation Timing API is a great 'tool' for debugging performance problems: <br/> [http://www.html5rocks.com/en/tutorials/webperformance/basics/ html5rocks.com/en/tutorials/webperformance/basics].

The API provides timing data for page load and navigation events, including DNS resolution and redirects. Data from the web.performance [http://analytics.blogspot.nl/2012/04/more-ways-to-measure-your-websites.html can be accessed via Google Analytics].

=== Performance checking ===

In order to avoid performance bugs, it crucial to incorporate performance checking in your workflow.

There are several tools for this.

'''Page Speed'''<br/> [https://developers.google.com/speed/pagespeed developers.google.com/speed/pagespeed]<br/> Google tool to 'help developers optimize their web pages by applying web performance best practices'. A similar tool is available from the Audit panel in the Chrome DevTools.

'''Blaze'''<br/> [http://www.akamai.com/blaze akamai.com/blaze]<br/> Akamai service for 'front end optimisation'.

W3C also offers a tool to check web pages for 'mobile friendliness': [http://validator.w3.org/mobile/ validator.w3.org/mobile].

== Browser and device capability ==

It's important to ensure that your target platforms support the HTML, JavaScript and CSS features you use, and to plan sensible fallback strategies. Several sites provide detailed, up-to-date information about this.

[http://www.caniuse.com caniuse.com]<br/> Mobile and desktop browser capabilities, with links to documentation

[http://mobilehtml5.org mobilehtml5.org]<br/> Capability information for mobile browsers.

[http://www.modernizr.com modernizr.com]<br/> Feature detection library supported by most web platforms.

[http://www.html5please.us html5please.us]<br/> HTML, CSS and JavaScript features: what's in flux, what's flakey, and what you can do about it.

[http://html5test.com html5test.com]<br/> [http://haz.io haz.io]<br/> Check HTML, CSS and JavaScript features supported by your browser.

[http://www.css3test.com css3test.com]<br/> Test for CSS3 feature support.

[http://www.jsperf.com jsperf.com]<br/> An easy way to create, run, compare and share JavaScript test cases.

[http://www.overlooksoft.com/fing overlooksoft.com/fing]<br/> Fing is a native app for checking the network environment – you can even run ping and traceroute.

== Reporting browser bugs ==

It's extremely important for the developer community that you report browser bugs as soon as you encounter them, however frustrating or trivial they may seem.

For more information about how to report bugs &ndash; and why you should do that &ndash; see [http://coding.smashingmagazine.com/2011/09/07/help-the-community-report-browser-bugs/ coding.smashingmagazine.com/2011/09/07/help-the-community-report-browser-bugs].

Simple bug reporting tool for Chrome for Android: [http://new.mcrbug.com new.mcrbug.com]

Safari: [https://developer.apple.com/bugreporter/ developer.apple.com/bugreporter]

Opera: [https://bugs.opera.com/wizard/ bugs.opera.com/wizard]

Firefox: [https://bugzilla.mozilla.org/ bugzilla.mozilla.org]

Internet Explorer: [http://connect.microsoft.com/ connect.microsoft.com]

== And finally... ==

Whatever you build, try to test it on a variety of mobile devices in a variety of contexts.

You don't need a complex test suite and usability lab for that: just get friends and colleagues to try out what you've built. [http://www.useit.com/alertbox/discount-usability.html Discount usability] is a lot better than none at all!

The mobile web is changing fast, unpredictably &ndash; what matters now may not matter in six months &ndash; so make sure to incorporate testing early in your workflow.

== Learn more ==

Brad Frost's guide to testing and tools:<br/> [http://mobilewebbestpractices.com/resources/#r-testing mobilewebbestpractices.com/resources/#r-testing]

Smashing Magazine articles about mobile web app design: <br/> [http://mobile.smashingmagazine.com/ mobile.smashingmagazine.com]

HTML5 Rocks articles about mobile web development: <br/> [http://www.html5rocks.com/en/mobile html5rocks.com/][http://www.html5rocks.com/en/mobile mobile]

Optimising mobile web app performance:<br/> [https://developers.google.com/speed/docs/best-practices/mobile developers.google.com/speed/docs/best-practices/mobile]

Ilya Grigorik on performance:<br/> [http://www.igvita.com/slides/2012/webperf-crash-course.pdf igvita.com/slides/2012/webperf-crash-course.pdf]

Brian Leroux on debugging mobile web apps: <br/> [http://brian.io/slides/debug-mobile/#/ brian.io/slides/debug-mobile]

Resources for finding information about web development, and how to help others: <br/> [http://movethewebforward.org/ movethewebforward.org]
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics|Developer Tools, Mobile}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}