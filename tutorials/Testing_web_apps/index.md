---
title: Testing web apps
attributions:
  - 'Facebook HTML5 Resource Center.'
readiness: 'Ready to Use'
summary: 'Now that you''ve built a web app, it''s important to test it so that you know users are getting the best experience possible. We''ve split this document into Mobile and Desktop, and provided information on some of the best tools out there to help you ensure your apps are built to the highest standards.'
tags:
  - Tutorials
  - Compatibility
  - Developer
  - Tools
uri: 'tutorials/Testing web apps'

---
## Summary

Now that you've built a web app, it's important to test it so that you know users are getting the best experience possible. We've split this document into Mobile and Desktop, and provided information on some of the best tools out there to help you ensure your apps are built to the highest standards.

## Mobile

### Which Browsers?

The mobile browser landscape changes much faster than that on the desktop, as devices are recycled much more quickly. This provides an opportunity for developers to develop against the latest APIs more rapidly than is possible on the desktop, but also means browser usage statistics are continuously changing.

We recommend that you choose where to focus your efforts based on the geographic markets that you're targeting. [StatCounter](http://gs.statcounter.com/) collects traffic usage data from over 3 million sites to provide up to date information which browsers are being used where.

The top mobile browsers for various geographies are shown in the charts below. This data is current as of May 2012.

<table>
<col width="50%" />
<col width="50%" />
<tbody>
<tr class="odd">
<td align="left"><h3>North America</h3>
<p><img src="/assets/public/2/20/mobile-stats-na-may.jpeg" alt="mobile-stats-na-may.jpeg" /></p></td>
<td align="left"><h3>Europe</h3>
<p><img src="/assets/public/1/11/mobile-stats-europe-may.jpeg" alt="mobile-stats-europe-may.jpeg" /></p></td>
</tr>
<tr class="even">
<td align="left"><h3>Australia</h3>
<p><img src="/assets/public/3/30/mobile-stats-aus-may.jpeg" alt="mobile-stats-aus-may.jpeg" /></p></td>
<td align="left"><h3>Asia</h3>
<p><img src="/assets/public/6/68/mobile-stats-asia-may.jpeg" alt="mobile-stats-asia-may.jpeg" /></p></td>
</tr>
<tr class="odd">
<td align="left"><h3>Africa</h3>
<p><img src="/assets/public/b/bf/mobile-stats-af-may.jpeg" alt="mobile-stats-af-may.jpeg" /></p></td>
<td align="left"><h3>South America</h3>
<p><img src="/assets/public/2/22/mobile-stats-south-america-may.jpeg" alt="mobile-stats-south-america-may.jpeg" /></p></td>
</tr>
</tbody>
</table>

### Ringmark

Each of these mobile browsers has different capabilities that may affect your app's performance. The open-source project Ringmark [[1]](http://rng.io/) provides a suite of tests that help you understand which browsers support the functionality your app needs; it also helps you learn what features you can expect your users to access now. Check out the [Ringmark section on Browserscope](http://www.browserscope.org/?category=ringmark&v=top-m) to see how specific mobile browsers stack up.

### Debugging

The plethora of mobile devices in the wild can make it very difficult to debug certain device-specific issues. There are a number of products out there to make your life easier.

[Device Anywhere](http://www.deviceanywhere.com/) host a large selection of mobile devices across multiple geographies and carriers. You control a device remotely to view, interact and debug your product on any number of handsets as either manual or automated tests.

#### iOS

Apple provides [simulators](https://developer.apple.com/devcenter/ios/index.action#downloads) for the iPhone, iPad and iPod touch. The built-in Safari browser has a [Developer mode](http://developer.apple.com/library/safari/#documentation/AppleApplications/Conceptual/Safari_Developer_Guide/2SafariDeveloperTools/SafariDeveloperTools.html) which reports errors and warnings more readily than the default setting.

#### Android

Google provides a cross-platform [emulator](http://developer.android.com/sdk/index.html) for vanilla versions of their Android operating system. In addition, calls to the JavaScript console are logged in the devices logcat system, where they can be read from an ADB shell. For more information on reading logcat logs see [this article](http://developer.android.com/guide/developing/debugging/debugging-log.html).

#### Windows Mobile

Microsoft provide emulators for a number of their mobile operating systems, including [Windows Phone 7](http://www.microsoft.com/download/en/details.aspx?id=13890) and [Windows Mobile 6](http://www.microsoft.com/download/en/details.aspx?displaylang=en&id=6135).

#### Blackberry

RIM provide simulators for every phone they've ever produced. Browse the full list [here](http://us.blackberry.com/developers/resources/simulators.jsp).

[Mobilexweb](http://www.mobilexweb.com/emulators) has a great article discussing the features of the various emulators and simulators with links to downloads and other useful information.

#### Opera

Opera has two distinct [mobile browsers](http://www.opera.com/mobile/new/) - Opera Mini and Opera Mobile. Opera Mini is a free browser that requests web pages via Operas servers, which reformat and compress the response (for example, images) for a faster download speed and more suitable output. Opera Mini can be run on a very wide range of feature and smart phones as well as tablets and other devices.

Opera Mobile is a browser that includes intelligent on-device reformatting technology. Opera Mobile also includes remote debugging of your mobile devices via [Dragonfly](http://dev.opera.com/articles/view/remote-debugging-with-opera-dragonfly/). Debug output from your mobile device can be viewed and modified on a desktop computer.

### Improving Performance

Performance in mobile applications is getting better and better, with browser vendors optimizing their products for the rich set of new APIs now available. However, there are still some pitfalls to avoid if you want your app to really sing. These tools will help you do that.

#### [Uber Bookmarklet](http://stevesouders.com/mobileperf/mobileperfbkm.php)

Steve Souders' really useful mobile performance [uber bookmarklet](http://stevesouders.com/mobileperf/mobileperfbkm.php) contains a number of tools for inspecting various aspects of your webapp while it's running on a mobile device. The suite includes [Firebug Lite](http://getfirebug.com/firebuglite) (DOM Inspector and Javascript Console), a resource counter, the [YSlow page analyser](http://developer.yahoo.com/yslow/), an automatic sprite generator and much more.

#### [Weinre](http://phonegap.github.com/weinre/)

Weinre is a remote web page debugger that allows you to inspect and modify both the DOM and Javascript runtime on one machine from another. This means you can debug your mobile webpage (running on a mobile device) on your desktop computer. Weinre reuses WebKit's [Web Inspector](http://trac.webkit.org/wiki/WebInspector) UI, so developers familiar with Chrome or Safari will feel right at home.

### Handling Many Screen Sizes

Since you're developing with web technologies, users will be able to access your app on various different devices with a number of different screen sizes. This requires your app to be able to handle several different screen sizes correctly. The easiest and best way to do that is to make your web app's width and height fluid so that it can fill the space that's available.

There are a number of live web apps that exhibit this when running on a touch-enabled device including [m.facebook.com](http://m.facebook.com), [m.flickr.com](http://m.flickr.com) and [mobile.nytimes.com](http://mobile.nytimes.com).

For a great tutorial on how you can pull this off, see [this article](http://woorkup.com/2010/01/10/best-practices-to-develop-perfect-websites-for-iphone-and-mobile-devices/).

CSS3’s [flexbox](http://coding.smashingmagazine.com/2011/09/19/css3-flexible-box-layout-explained/) layout model makes it much easier to handle a wide range of screen sizes by providing easier to understand control over which parts of your application should be fixed and flexible widths. Browser support is getting better all the time. An up-to-date compatibility table can be found at [CanIUse.com](http://caniuse.com/#feat=flexbox).

## Desktop

### Which Browsers?

The surface area for testing on desktop is much smaller than on mobile, but the difference in features betwen the major browers tends to be larger than with mobile browsers. This is because desktop browsers have traditionally had significantly longer half-lives than their mobile counterparts.

Browser usage differs considerably around the globe, so it's a good idea to check on stats for the geographies you're targeting with your application. The data below is current as of May 2012.

<table>
<col width="50%" />
<col width="50%" />
<tbody>
<tr class="odd">
<td align="left"><h3>North America</h3>
<p><img src="/assets/public/a/ab/browsers-na-may.jpeg" alt="browsers-na-may.jpeg" /></p></td>
<td align="left"><h3>Europe</h3>
<p><img src="/assets/public/4/48/browsers-eu-may.jpeg" alt="browsers-eu-may.jpeg" /></p></td>
</tr>
<tr class="even">
<td align="left"><h3>Australia</h3>
<p><img src="/assets/public/9/90/browsers-au-may.jpeg" alt="browsers-au-may.jpeg" /></p></td>
<td align="left"><h3>Asia</h3>
<p><img src="/assets/public/9/9a/browsers-asia-may.jpeg" alt="browsers-asia-may.jpeg" /></p></td>
</tr>
<tr class="odd">
<td align="left"><h3>Africa</h3>
<p><img src="/assets/public/f/f8/browsers-africa-may.jpeg" alt="browsers-africa-may.jpeg" /></p></td>
<td align="left"><h3>South America</h3>
<p><img src="/assets/public/4/4d/browsers-sa-may.jpeg" alt="browsers-sa-may.jpeg" /></p></td>
</tr>
</tbody>
</table>

#### Internet Explorer

IE9 and IE8 both come with pre-installed [Developer Tools](http://msdn.microsoft.com/en-us/ie/aa740478) (for IE6 and 7, the Developer Tools are available as a separate download). The latest version provides the developer with tools to inspect and edit the live DOM and profile your JavaScript code.

#### Chrome

Chrome is based on the WebKit rendering engine, which provides a comprehensive suite of developer tools via the [WebInspector](http://trac.webkit.org/wiki/WebInspector) project. WebInspector gives access to the live DOM, the JavaScript runtime for script debugging and profiling, resource inspection and network analysis.

#### Firefox

Most developers debug in Firefox with [Firebug](http://getfirebug.com/). Similar in many ways to the WebKit WebInspector, Firebug provides a full-featured toolbox for debugging the most complex web applications.

#### Safari

Like Chrome, Safari is based on the WebKit rendering engine and comes with [WebInspector](http://trac.webkit.org/wiki/WebInspector) pre-installed.

#### Opera

Modern versions of Opera come pre-installed with [Dragonfly](http://www.opera.com/dragonfly/). Similar to Firebug and WebInspector, Dragonfly has a few unique features like remote debugging for non-Desktop devices and a request crafter.

#### Plugins

Many desktop browsers have a plugin architecture which allows third party developers to provide additional capabilites for the browser. The following are useful for testing purposes. Please note, not all plugins are available for all browsers.

-   Google [PageSpeed](http://code.google.com/speed/page-speed/). Available for Google Chrome and as a standalone webapp, PageSpeed analyses your application and suggests areas where performance could be improved.
-   [YSlow](http://developer.yahoo.com/yslow/) from Yahoo! is similar to PageSpeed and available for Chrome, Firefox, Opera and as a bookmarklet (useful for mobile).

### Handling Old Browsers

Users will be accessing your web app with a variety of browsers including Chrome, Firefox, IE, Safari (mostly mobile), and Android's browser. On mobile and in America and Europe, the majority of users will likely be accessing your web app using a Webkit-enabled browser, meaning that features available will be very similar. In Asia, Opera Mobile is very popular. Desktop is more bifurcated. IE, Chrome, and Firefox run different engines and each have significant slices of the market.

A large portion of users on the internet are running the newest browsers, but there are pockets of users who are using browsers that don't support the latest features. In order for the user to have the best experience possible, you'll want to detect which features are available within the browser. The best way to do that is by using libraries, like these.

### [Modernizr](http://www.modernizr.com/)

Modernizr is an open-source Javascript library that simplifies feature testing browsers for HTML5 and CSS3 support. It exposes functionality to easily allow you to detect if the user's browser supports a particular feature (like the `canvas` element, for example). You can download it [here](https://github.com/Modernizr/Modernizr).

### [YepNope](http://yepnopejs.com/)

Yepnope is an asynchronous conditional resource loader that's super-fast, and allows you to load only the scripts that your users need. Download it [here](https://github.com/SlexAxton/yepnope.js).

### [CanIUse](http://caniuse.com)

CanIUse.com is a valuable resource to check on the current support for HTML5 features in browsers, including mobile. If you would like to understand how to detect features on your own, see [Dive Into HTML5](http://diveintohtml5.org/everything.html).

If you know in advance specific browsers you need to target, there are also some great resources cataloging the features and performance of the major browsers.

### [QuirksMode.org](http://www.quirksmode.org)

QuirksMode.org is a great source for browser compatibility information and home to accurate and up-to-date browser [compatibility tables](http://www.quirksmode.org/compatibility.html) for JS and CSS.

### [Browserscope](http://www.browserscope.org)

Browserscope is a community driven project for profiling web browsers 'in the wild', covering performance metrics over range of standards.

## Test Frameworks

Many of the modern HTML5 application frameworks come with their own test frameworks built in (for example jQuery's [Qunit](http://docs.jquery.com/Qunit)), but there are also a number of independent frameworks out there worth a mention.

### [Selenium](http://seleniumhq.org/)

Selenium is a browser automation framework which can be used to automate navigation through user flows in your application. This is especially useful to protect against regressions when you push code and running liveness tests.

The WebDriver project defines the core APIs used by Selenium to control the browser. Unlike many other browser automation frameworks it allows tests to interact with each browser at a lower level than the DOM, ensuring your test cases closely mimic the actions of real users. WebDriver is available as a stand alone product and is used by a variety of projects.

### [JS TestDriver](http://code.google.com/p/js-test-driver/wiki/GettingStarted)

JS TestDriver brings [Test-driven Development](http://en.wikipedia.org/wiki/Test-driven_development) to your JavaScript workflow and is most useful when you have business logic running on the client. It integrates well with a number of common IDEs including Aptana, Eclipse and IntelliJ.

### [Jasmine](http://pivotal.github.com/jasmine/)

Jasmine is a [Behavior-driven Development](http://en.wikipedia.org/wiki/Behavior_Driven_Development) Javascript framework without any external dependencies or requirements. Like JS TestDriver, Jasmine does not operate on the DOM and is most useful for testing business logic running in the browser.

### [YUI Library](http://developer.yahoo.com/yui/)

YUI's test harness is a very solid unit testing tool of the xUnit family. It can be used outside of YUI Library itself. It supports asynchronous testing and has rock solid export tools.

### [Ripple](http://ripple.tinyhippos.com/)

Ripple is a Google Chrome browser extension that lets you test your mobile web app in multiple environments in minutes. It's a very simple and powerful tool.
