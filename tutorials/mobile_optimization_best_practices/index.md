---
title: 'Mobile optimization best practices'
attributions:
  - 'Facebook HTML5 Resource Center.'
readiness: 'Ready to Use'
summary: 'Mobile Devices may have slow network connections, hardware specific limitations and varying screen sizes. We need standardized best practices for building web apps. The goal is to provide the best user experience optimizing the HTML5 standards.'
tags:
  - Tutorials
  - JavaScript
  - Mobile
  - Performance
uri: 'tutorials/mobile optimization best practices'

---
## Summary

Mobile Devices may have slow network connections, hardware specific limitations and varying screen sizes. We need standardized best practices for building web apps. The goal is to provide the best user experience optimizing the HTML5 standards.

## Network Speed Optimizations

At times, a phone or tablet's connection to the internet can be slow or spotty, so it's important to prepare for those types of conditions. We highly recommend that you familiarize yourself with the html5/build/richui key concepts of a web app, especially the concept of heavily relying on AJAX to load only data and not HTML mark up, beyond the first page load.

If you follow that practice, coupled with the practices below, it is easier to build around a slow or spotty network connection.

### Cache data locally

The HTML5 spec introduces offline capabilities, with the fringe benefit of being able to heavily locally cache your apps' static resources (image, scripts, css, etc).

### Compress and Minimize Data

Ensure that you're compressing all data that's sent over the wire by using gzip. You can also minify HTML, CSS, and JavaScript files.

### Cookies

Only rely on cookies if that's the only option available. Place your static resources in a URI path, domain, or sub-domain where cookies will not be sent. So if you are hosting your dynamic page from www.example.com and setting cookies for this, you could host your images in images.example.com and when setting the initial cookies, restrict them to the www.example.com domain.

### Manage requests

Batch your server requests where possible. It is also recommended that you make fewer requests for external resources (scripts, images, style sheets, etc.) that have more data than making many requests with less data. This approach lends itself to using image sprites or combining scripts. You will also want to eliminate redirects. If you require redirects try to limit these to at most two, and do this server-side to minimize client-side round trip delays.

### Lazy loading

Only load resources when needed. For example, you can make use of the [YepNope](http://yepnopejs.com/) JavaScript library to load only the desired scripts you need for certain browsers. This library is usually used with [Modernizr](http://www.modernizr.com/) to load the desired JavaScript library based on features a browser supports. Also, we recommending pre-loading resource before the user navigates to them so that they'll load instantly.

### Images

You can add images inline as base64 encoded strings and use CSS to display these. This avoids an HTTP request but the inline image data representation is bigger (about 30%). The recommended practice is to use this for smaller images. You should also cache dynamic images that do not change much (e.g. profile pictures). You can generate these cached images by hashing the resource content and including the hash in the name. This content can then be stored on the server. When the content changes, the image reference changes and the new image is pulled down by the browser. Lastly, you can make use of image sprites (a collection of images in one) to minimize the number of images transferred. You would then use CSS to display a desired individual image.

## App Speed

The speed of an app, and how your user perceives it, factors into user satisfaction with your app. There are some optimizations you can make to make your app fast.

### Local caching of dynamic data

You can cache data locally which will serve to speed up the app.

### Caching static files

You can use AppCache to cache static files and this will optimize the initial load time of your app.

### Place JavaScript at the bottom

You want to place all your JavaScript at the bottom of the page. This will optimize the perceived latency because as the page is loaded it stops upon encountering JavaScript. Putting scripts at the bottom allows the user interface to display before the JavaScript is loaded.

### Use progress bars

While it won't make your app faster, it will give the user feedback as to what's happening.

### Avoid page reloads

Instead, make use of AJAX to load only the views that are changing. Where possible, you should pre-load pages to increase the perceived speed of your app.

## Device Features

There is a wide range of mobile browsers, each with different screen sizes, screen resolutions, and support for different HTML features. Based on your target audience, you will want to optimize the user experience based on device features.

### Viewport

The viewport metadata provides the browser with information on how the content should fit on the device screen.

    <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">

The `width` property controls the size of the viewport. It can be set to a specific number of pixels like `width=600` or to the special value device-width value which is the width of the screen in CSS pixels at a scale of 100%. (There are corresponding height and device-height values, which may be useful for pages with elements that change size or position based on the viewport height.)

The initial-scale property controls the zoom level when the page is first loaded. The ` maximum-scale, minimum-scale, and user-scalable ` properties control how users are allowed to zoom the page in or out.

### HTML5 feature support

HTML5 compatibility varies across browsers. [Ringmark](https://developers.facebook.com/html5/blog/post/2012/02/27/announcing-ringmark--a-mobile-browser-test-suite/) is an open-source test suite that allows you to see which browsers have the functionality you need to build on. A comparison of results for different mobile browsers is available on [Browserscope](http://www.browserscope.org/?category=ringmark&v=top-m).

To optimize the experience for non-supporting browsers you can make use of [Modernizr](http://www.modernizr.com/) and [YepNope](http://yepnopejs.com/) JavaScript libraries to detect feature support and setup fallback methods.

### CSS Media Queries

You can load style sheets that depend on device characteristics (orientation, size, resolution) through the use of a media query. For example the following will load a specific style sheet for devices with screen sizes between 641 and 800 pixels in width.

    <link rel="stylesheet"
      media="only screen and (min-width: 641px) and (max-width: 800px)"
      href="medium_width.css">

## User Experience

You can optimize the mobile user experience based on characteristics unique to the mobile environment in general. This includes considering the challenges of inputting data on mobile devices, smaller screens, and any other user experience improvements.

### Screen optimization

Your content should flow well regardless device orientation and screen sizes. You should use fluid width when designing your web app, which means using percentages or relative measurements instead of absolute pixels. You should also auto-hide the address bar so you can recover some space at the top. That can be done by using this code:

    <body onload="setTimeout(function() { window.scrollTo(0, 1) }, 100);"></body>

### Interaction methods

Mobile devices have three main interaction methods; focus, pointer, and touch. For example, the iPhone is mainly touch based while some older BlackBerry phones are pointer based. When you design your user interface you want to pay attention to the input methods, for example in touch-based devices you want more space around unique interaction points to avoid mistakes due to "fat-fingering".

### Home screen icons

You can provide shortcuts for your web apps that can be place in the devices' home screens. You can do this for iOS and Android through \`link\` tags, example:

    <link rel="apple-touch-icon" href="/icons/ios_icon.png" />
    <link rel="apple-touch-icon-precomposed" href="/icons/android_icon.png" />

You can also upsell the user to this functionality by using the open source [Bookmark Bubble](http://code.google.com/p/mobile-bookmark-bubble/).

## Mobile Carriers

Some mobile networks employ minification and compression techniques on data that is sent over a mobile network to a device. This only applies when the device is using a mobile data connection such as LTE, 3G or GPRS. External resources, such as scripts and images, may not be delivered to the client device as the developer intended. Large libraries can be broken by the techniques employed by carriers. Here's an article discussing this issue, which also offers a solution should you need one. \* [[1]](http://stuartroebuck.blogspot.co.uk/2010/08/official-way-to-bypassing-data.html)

## Additional Resources

-   [Mobile Web App Best Practices](http://www.w3.org/TR/mwabp/)
-   [Page Speed - Optimize for mobile](http://code.google.com/speed/page-speed/docs/mobile.html)
-   ["Mobifying" Your HTML5 Site](http://www.html5rocks.com/en/mobile/mobifying.html)
-   [Browser compatibility - viewports](http://www.quirksmode.org/mobile/tableViewport.html)
