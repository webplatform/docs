---
title: Detecting device and browser
tags:
  - Guides
  - Mobile
readiness: 'Ready to Use'
summary: 'This article explains client and server-side techniques for detecting browser capabilities.'
uri: 'concepts/Detecting device and browser'

---
# Detecting device and browser

## Summary

This article explains client and server-side techniques for detecting browser capabilities.

Device detection enables developers to identify device properties and characteristics in order to determine the best content, layout, mark-up or application to serve to a given device. These characteristics include screen size, browser type and version, media support, and the level of support for CSS, HTML and JavaScript.

## Why use device and feature detection?

The ability to identify a device, browser or feature enables the developer to perform actions such as:

-   Serve a mobile formatted site rather than the desktop site.
-   Swap style sheets to adapt layout and content to the device’s specific HTML, CSS and JavaScript capabilities.
-   Modify the amount or nature of content to suit device capabilities. For example, a JavaScript-based slide show may be served to a higher-end device, and a simple list served to a lower-end device.
-   Serve smaller or larger images to suit screen size, or swap SVG graphics for bitmap images on less capable devices.
-   Enhance functionality on more capable devices by applying progressive enhancement based on feature and object detection.
-   Increase or decrease font size, margins and padding to scale the actionable areas on a touch device.
-   Serve different sizes and/or formats of media such as video to suit device codecs or capabilities.

## Common approaches to device detection

Device detection can be accomplished server-side, before content is delivered to the client, or client-side, after content and related files have been loaded to the device itself. Both approaches have advantages and disadvantages, which are described in this topic. Smartphone browsers generally have better client-side detection capabilities than cheaper feature phones, and this gives Web developers more flexibility to use design techniques such as the responsive design approach. Feature phone browsers are designed to provide speed, performance and bandwidth optimization, but may lack advance features required for some design approaches.

## Client-side detection

Client-side detection employs JavaScript to detect the type of browser, as well as using DOM objects and properties such as screen.width, screen.pixelDepth, navigator.userAgent, and navigator.cookieEnabled. Using CSS, it is now also possible to implement 'progressive enhancement', which is a design strategy to enable any browser to access the basic content of a Web page, while serving the complete feature set of the page to those browsers that support advanced technologies. For more information on progressive enhancement, see [Wikipedia](http://en.wikipedia.org/wiki/Progressive_enhancement), [A List Apart](http://www.alistapart.com/articles/understandingprogressiveenhancement/) and [modernizr.com](http://modernizr.com/).

Media queries are another common strategy for adapting content to a device, based on media type and device width or display size. For more information on media query techniques, see [Creating a Mobile-First Responsive Web Design](http://www.html5rocks.com/en/mobile/responsivedesign/) and [Mobifying Your HTML5 Site](http://www.html5rocks.com/en/mobile/mobifying/) on HTML5 Rocks.

### Advantages of client-side detection

The main advantage of client-side detection is the ability to react promptly to exact client conditions such as size, orientation, and accurately assess support for specific elements and APIs. Capability detection is developed and executed purely on the client, using CSS and JavaScript. There is no requirement for web servers to provide device detection or serve alternative content, and installation and maintenance of a device database is not required.

Client-side detection can provide a useful fallback and can implement run-time tweaks in response to behavior such as changes in device orientation. On more advanced devices, client-side Ajax and CSS can be used to download additional content and enhancements without having to refresh an entire page.

### Disadvantages of client-side detection

When incorrectly implemented, client-side detection may cause a device to request content that is unsupported. In this case, a user will be notified that the browser is not capable of rendering the content only after time and bandwidth have been wasted delivering it. Because JavaScript and CSS execute locally, an entire page may have to be downloaded before scripts can process and manipulate the Document Object Model [DOM](http://en.wikipedia.org/wiki/Document_Object_Model). In addition, JavaScript and media queries are not supported on some older devices, and there may be a time lag between page load and execution of client-side adaptation.

## Server-side detection

Server-side detection of devices and capabilities is usually performed by analysing HTTP request headers received from the client (also called the user agent). In most cases, only the User-Agent string is needed, but sometimes a combination of more than one header is required.

For more information about specific server-side detection techniques, see:

-   [Server-Side Detection: History, Benefits and How-To](http://mobile.smashingmagazine.com/2012/09/24/server-side-device-detection-history-benefits-how-to/)
-   [A Non-Responsive Approach to Building Cross-Device Webapps](http://www.html5rocks.com/en/mobile/cross-device/).

### Advantages of server-side detection

The main advantages of server-side detection are that it saves client resources and does not rely on the ability of the client to adapt the content that it receives. As soon as the client makes a request, server-side applications learn the identity of the device and what it can do. This makes it possible to serve only media and content that is most appropriate for that particular device. For example, if a mobile device is old and has a small screen, it will not be served a page section displaying HD video.

Server-side detection enables optimization of assets such as CSS files, CSS image sprites, scripts, and so on. It can be extremely efficient when combined with device or 'group-based' caching on the server. For an example of a group-detection script, see [WordPress Mobile Pack](http://wordpress.org/extend/plugins/wordpress-mobile-pack/)'s device group detection script.

### Disadvantages of server-side detection

Databases for server-side detection require frequent updating, are not always accurate, and do not respond to user settings or personalization. Employing a device database requires implementing a server-side API and maintaining it. (The simplest solution is to employ a short script containing only very basic information, such as the one shown in WordPress Mobile Pack's lite-detection php script.)

## Best of both worlds

Server-side and client-side detection techniques can be used together to enable the developer to only serve content that is supported by a device, while allowing the browser to adjust style and layout in response to the current context.

Note: This material was originally published as part of the Nokia Developer Web Development Library, available as [Device and browser detection](http://www.developer.nokia.com/Resources/Library/Web/#!nokia-browsers/common-elements-of-nokia-browsers/device-and-browser-detection.html)

## See also

### External resources

[http://www.developer.nokia.com/Community/Wiki/index.ph/Device\_and\_feature\_detection\_on\_the\_mobile\_web](http://www.developer.nokia.com/Community/Wiki/index.ph/Device_and_feature_detection_on_the_mobile_web)

[http://mobiforge.com/developing/story/lightweight-device-detection-php](http://mobiforge.com/developing/story/lightweight-device-detection-php)

[http://yiibu.com/articles/rethinking-the-mobile-web/](http://yiibu.com/articles/rethinking-the-mobile-web/)

[http://mobiforge.com/designing/story/effective-design-multiple-screen-sizes](http://mobiforge.com/designing/story/effective-design-multiple-screen-sizes)

[http://mobiforge.com/designing/story/a-very-modern-mobile-switching-algorithm-part-i](http://mobiforge.com/designing/story/a-very-modern-mobile-switching-algorithm-part-i)

[http://calendar.perfplanet.com/2010/high-performance-mobile/](http://calendar.perfplanet.com/2010/high-performance-mobile/)

[http://www.cloudfour.com/css-media-query-for-mobile-is-fools-gold/](http://www.cloudfour.com/css-media-query-for-mobile-is-fools-gold/)

To access screensize with JS is tricky in mobile: [http://tripleodeon.com/2011/12/first-understand-your-screen/](http://tripleodeon.com/2011/12/first-understand-your-screen/)

