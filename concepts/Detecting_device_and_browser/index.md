{{Flags}}
{{Summary_Section}}
{{Guide
|Content=Device detection enables developers to identify device properties and characteristics in order to determine the best content, layout, mark-up or application to serve to a given device. These characteristics include screen size, browser type (or version), media support, and the level of support for Cascading Style Sheets (CSS), HTML and JavaScript technology.

== Why use device and feature detection? ==

The ability to identify a device, browser or feature enables the developer to perform actions such as:

* Serving a mobile formatted site rather than the desktop site.
* Swapping style sheets to adapt layout and content to the device’s specific HTML, Cascading Style Sheets (CSS) and JavaScript technology capabilities.
* Modifying the amount or nature of content to suit the device capacity. For example, a JavaScript based slide show may be served to a higher-end device, and a simple list served to a lower-end device.
* Serving smaller or larger images to suit screen size, or swap SVG graphics for bitmap images on less capable devices.
* Enhancing functionality on more capable devices by applying progressive enhancements (based on feature and object detection).
* Increasing or decreasing font size, margins and padding to scale the actionable areas on a touch device.
* Serving different sizes and/or formats of media such as video to suit the device codecs or capabilities.

== Common approaches to device detection ==

Device detection can be accomplished server-side, before the content is delivered to the client, or client-side, after the content and related files have been loaded to the device itself. Both approaches have advantages and disadvantages, which are described in this topic. Depending on the browser features, smartphone browsers are generally more capable to better client-side detection and give more flexibility to Web developers to apply different design approaches, for example responsive design approach. On the other hand, many feature phone browsers are designed to provide speed, performance and bandwidth optimization, and may lack advance features to handle certain design approaches.

== Client-side detection ==

Client-side detection employs JavaScript technology to detect the type of browser as well as DOM objects and properties such as screen.width, screen.pixelDepth, navigator.userAgent, and navigator.cookieEnabled. Using CSS, it is now also possible to implement “progressive enhancement”, which is a Web design strategy that enables every browser to access the basic content of a Web page, serving the complete feature set of the page only to those browsers that support advanced technologies. For more information on progressive enhancement, see Wikipedia, Dev,Opera, and A List Apart.

Media queries are another common strategy for adapting content to a device based on media type and device width or display size. For more information on media query techniques, see Client-side detection of Nokia devices.

Advantages of client-side detection

The main advantage of client-side detection is the ability to react promptly to exact client conditions such as size, orientation, and support for extra tags and APIs. It is simple to execute using a combination of JavaScript and CSS and is an integral part of the Web page design; there are no requirements for Java, PHP, .NET software to dynamically modify your Web pages. Another advantage is that installing and maintaining a database is not required.

Client-side detection can provide a useful fallback and can implement last-minute tweaks related to real-time behavior such as changes in device orientation. On more advanced devices, client-side Ajax and CSS can be used to download additional content and enhancements without having to refresh the entire page.

Disadvantages of client-side detection

One disadvantage of client-side detection are is that it often runs the risk of sending content that is not supported by the device. The user is notified that the browser is not capable of rendering the content only after time has been wasted delivering it. Because JavaScript and CSS execute locally, the entire page may download before the script can process and manipulate the Document Object Model (DOM). Another disadvantage is that JavaScript and media queries are not supported on older devices. A third disadvantage is the time lag that elapses between the initial loading and the execution of the client-side adaptation.

== Server-side detection ==

Server-side detection is usually performed by analysing the HTTP request headers received from the client (also called the user agent). In most cases, only the User-Agent string is needed, but sometimes a combination of more than one header is required.

Server-side detection requires a database of User-Agent strings (and other headers, if needed) associated with a list of devices and capabilities. Mobile-device databases range from the very simple, which provide limited data, to the very detailed, which require more resources and are complicated to implement. An example of a very simple device database is the lite-detection.php script included in the WordPress Mobile Pack, which recognises a mobile device from a common PC. Online services such as {???} can generate a script for you, based on some simple rules that you can define on their Web site.

More complex databases contain details about display size, supported markup, AJAX, Flash, and so on. There are many types of device databases on the market; some are open-source, some are free, and some are commercial. Some examples are WURFL, DeviceAtlas, Microsoft’s Mobile Device Capabilities, and DetectRight.

For more information about specific server-side detection techniques, see Server-side detection of Nokia devices.

Advantages of server-side detection

The main advantages of server-side detection are that it saves client resources and it does not rely on the ability of the client to adapt the content that it receives. As soon as the client makes the request, you learn the identity of the device and what it can do. You can then serve only the media and content that is most appropriate for that particular device. For example, if you find out that the mobile device is old and has a small screen, you will not show it the HD video section.

Server-side detection enables optimization of assets such as CSS files, image sprites, scripts, and so on. It can be extremely efficient when combined with device or group-based caching on the server. For an example of a group-detection script, see WordPress Mobile Pack's device group detection script.

Disadvantages of server-side detection

The disadvantages of server-side detection are that the databases require frequent updating, are not always accurate, and do not include user settings or personalizations. Employing a device database requires implementing an API and maintaining it. The simplest solution is to employ a short script containing only very basic information, such as the one shown in WordPress Mobile Pack's lite-detection php script.


== Best of both worlds ==

Server-side and client-side detection techniques can be used together to enable the developer to drop content that is not supported by the device while allowing the browser to take care of applying the correct style and layout depending upon the current context.

Note: This material was originally published as part of the Nokia Developer Web Development Library, available as [http://www.developer.nokia.com/Resources/Library/Web/#!nokia-browsers/common-elements-of-nokia-browsers/device-and-browser-detection.html Device and browser detection]
}}
{{See_Also_Section
|External_links=http://www.developer.nokia.com/Community/Wiki/index.ph/Device_and_feature_detection_on_the_mobile_web

http://mobiforge.com/developing/story/lightweight-device-detection-php

http://yiibu.com/articles/rethinking-the-mobile-web/

http://mobiforge.com/designing/story/effective-design-multiple-screen-sizes

http://mobiforge.com/designing/story/a-very-modern-mobile-switching-algorithm-part-i

http://calendar.perfplanet.com/2010/high-performance-mobile/

http://www.cloudfour.com/css-media-query-for-mobile-is-fools-gold/
}}
{{Topics|Mobile}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}