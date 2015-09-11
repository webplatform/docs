---
title: HTML5 hybrid applications
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
readiness: 'Ready to Use'
summary: "A hybrid app is a native mobile app that is built using the web platform that uses a native ‘shell’ to wrap the web content.\_ Hybrid apps are installed through an app store, run on the device and provide access to enhanced native device hardware, but are written primarily using HTML, CSS and JavaScript. \_Instead of using the native SDK to create the application, hybrid apps typically wrap a web application with a native web view controller full screen, without the address bar or other normal browser controls."
tags:
  - Concept
  - Pages
  - Mobile
uri: 'concepts/Internet and Web/html5 hybrid applications'

---
## <span>Summary</span>

A hybrid app is a native mobile app that is built using the web platform that uses a native ‘shell’ to wrap the web content.  Hybrid apps are installed through an app store, run on the device and provide access to enhanced native device hardware, but are written primarily using HTML, CSS and JavaScript.  Instead of using the native SDK to create the application, hybrid apps typically wrap a web application with a native web view controller full screen, without the address bar or other normal browser controls.

# <span>What is a hybrid mobile app?</span>

A hybrid app is a native mobile app that uses a native ‘shell’ to wrap web content.  Hybrid apps are installed through an app store, run on the device and provide access to enhanced native device hardware, but are written primarily using HTML, CSS and JavaScript.  Instead of using the native SDK to create the application, hybrid apps typically wrap a web application with a native web view controller full screen, without the address bar or other normal browser controls.

Frameworks like Cordova (formerly PhoneGap) or Titanium have made development of hybrid apps much simpler by providing an easy-to-use template for the native app and a web-to-native abstraction layer that allows JavaScript access to the native APIs provided by the platform.

# <span>Why does building a hybrid app makes sense?</span>

There are many reasons why building a hybrid application makes sense, such as native app store distribution, or access to native APIs that aren’t available to mobile web apps.

-   **Use the skills you know and have today** - If you’re already an accomplished web developer, building a hybrid app requires a short and easy-to-achieve learning curve, and there are no new languages to learn.
-   **Distribution through native app stores** - Because hybrid apps use the native SDK to wrap the web app, they can be distributed through the native app store, making discovery and distribution easier for users.
-   **Access to native APIs** - The web-to-native abstraction layer provided by hybrid frameworks provides JavaScript access native APIs and capabilities that are not available to mobile web apps.
-   **Runs locally on the device, and works when offline** - Hybrid apps can package the required HTML, CSS and JavaScript within the app that’s installed through the app store, which means they run locally on the device and do not depend on a network connection to function.
-   **Uses a shared code base across multiple platforms** - Using HTML, CSS and JavaScript to build a hybrid app makes it easy to share the majority of code between different platforms.  While there may be some differences between the rendering, it is no different than having to support multiple browsers.
-   **Fast development time** - If you already have an existing web app, or code base that is built on the web platform, building a hybrid app is typically faster than writing an app using the native SDK, and because of the ability to share code between platforms, significant time is saved through code reuse.

# <span>What are the drawbacks of building a hybrid app?</span>

Hybrid apps do have some drawbacks compared to native apps or web apps, and you must decide if those drawbacks outweigh the benefits of writing a native app.

-   **Performance** - Hybrid apps may feel slower than a native app or a web app running in the browser because the JavaScript engine’s just-in-time compilers may be disabled by the operating system, in particular on [iOS](http://daringfireball.net/2011/03/nitro_ios_43).
-   **Differences in platforms** - Like mobile web apps, hybrid apps use the native web rendering engine on the device, which means that there may be subtle differences between the way content is rendered.  For example, when editing an \<input type="date"\>, the native date-picker may be provided by one device, but not by another.
-   **Creating consistent user interfaces** - Every platform has its own look and feel, and offers a set of pre-styled controls that developers can easily take advantage of.  Mimicking those controls is exceedingly difficult.
-   **Distributing an update** - Updating a mobile web app has a nearly instant return, once your app is uploaded, anyone using it is using the latest version.  With hybrid apps, you must upload your app to the app store, wait for it to be approved and then wait as users upgrade from their current version to the newest version.
-   **Instant access to new platform features** - Native apps will typically have access to new SDK features faster than what’s available to hybrid apps.  It takes some time for the abstraction layer to be written and made available to developers to use.

# <span>How to get started building a hybrid app</span>

1.  **Choose the hybrid framework that works best for you** - There are several framework choices available, the most popular is Cordova.  It’s an open source project with a strong community and plenty of resources available to help get you going.  Porting an existing mobile web app to a hybrid app with Cordova is pretty straightforward.  Other frameworks like Titanium may require significant rewriting, but will provide a more native feel.
2.  **Write your app** - Whichever framework you choose to use, writing a hybrid app isn’t much different than writing a mobile web app.  You should use all of the best practices for building mobile web apps, including CSS3 transitions, transforms and animations for any animations you plan on doing.  One strategy is to provide both a native app experience and a web experience for those who cannot install the app.
3.  **Optimize and test your app for each platform you plan to ship on** - Making your app look and feel like a true native app is difficult, but optimizing your app for each platform you plan to ship on will help to improve the user experience.  Just like you would never deploy your web app without testing it on the major platforms, you should do the same for your hybrid app.  Beyond testing different devices, be sure you test all of the different operating system versions as well.
4.  **Upload the app to the app store** - Once you’ve tested your app and you’re ready to distribute it, upload it to the app store.  Each store has a different process to upload, review and make your app available to users.

## <span>See also</span>

### <span>Other articles</span>

[PhoneGap](http://docs.webplatform.org/wiki/mobile_web/PhoneGap)

### <span>External resources</span>

<li>
[PhoneGap](http://phonegap.com/)

</li>
<li>
[Cordova](http://incubator.apache.org/cordova/)

</li>
<li>
[Titanium](http://www.appcelerator.com/platform/titanium-sdk/)

</li>
<li>
[Featured PhoneGap apps](http://phonegap.com/app/feature)

</li>
<li>
[10 tips for getting that native iOS feel with PhoneGap](http://www.mikedellanoce.com/2012/09/10-tips-for-getting-that-native-ios.html)

</li>
