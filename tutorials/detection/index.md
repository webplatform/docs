---
title: Feature, Browser, and Form Factor Detection: It's Good for the Environment
readiness: 'Ready to Use'
summary: 'This article is about tuning your app to the environment it''s running in, focusing on the specific challenge of detection. In other words, surveying the environment you''re running in.'
tags:
  - Tutorials
  - Design
uri: tutorials/detection

---
**By Michael Mahemoff**
Originally published June 27, 2011

## <span>Summary</span>

This article is about tuning your app to the environment it's running in, focusing on the specific challenge of detection. In other words, surveying the environment you're running in.

## <span>Overview</span>

This article is about tuning your app to the environment it's running in, focusing on the specific challenge of detection. In other words, surveying the environment you're running in. Three techniques are covered:

-   Feature detection, to decide if a particular feature is supported.
-   Browser detection, to decide which browser you're running in.
-   Form factor detection, to decide which form factor you're running in (smartphone, TV, etc.).

## <span>Background</span>

HTML5 is everywhere these days. Whether desktop or mobile, windows or Mac, or just about any other modern form factor and operating system, you will find an HTML5-savvy web browser. In fact, you will probably find several. This is great news for users, who benefit from browsers competing on features like speed and security and receive a consistent experience across different apps.

But how about the developer experience? On the whole, a ubiquitous platform is a positive story for developers, allowing them to target many different environments with the same code base.

If the web's promise of "write once, run many" sounds too good to be true, that's because it *is* too good to be true. The catch is that no two environments are entirely alike, and some of them are very different. A shiny new Google TV running Chrome is very different from a legacy mobile running Opera Mini, a browser designed to reduce bandwdith and processing requirements. We want our apps to be good for the environment, whatever the environment, and this behooves us to tailor them accordingly.

Fortunately, the web has always worked this way. In many respects, its success derives from environmental versatility, a goal that has always been at the heart of of web standards and web development techniques. Broadly speaking, there are two types of technique: "work out what environment we're in," followed by "now do something for this kind of environment". This article focuses on "work out what environment we're in". It's a detection problem, so put on your detective hat and let's get sleuthing ….

## <span>Feature Detection</span>

Feature detection is the most popular technique among the three we'll examine in this article. Simply put, detect if a feature exists. If so, use it; if not, don't...and hopefully fall back to something sensible. For example:

    detectCanvas() ? showGraph() : showTable();

Simple enough. But how do we actually *detect*? That is, how do we decide if the current environment supports the [en/tutorials/\#canvas canvas element]? There's no magic way to answer questions like this; browsers don't offer built-in feature detection APIs (yet), so it really is a detective effort. You look around for clues in the environment and make a call, even if you're not 100% certain.

In the case of canvas detection, one way is to create a canvas element and see if it supports a known property of canvas, the `getContext` method:

    function detectCanvas() {
      var canvas = document.createElement("canvas");
      return canvas.getContext ? true : false;
    }

You might wonder why we need the second line. Isn't it enough to just create a canvas element? In fact, browsers will let you create unknown DOM elements. The only way to know if the canvas is legitimate is to test if it actually behaves like a canvas. That's detective work!

Our canvas detection is an example of a more general pattern for feature detection: "Create a DOM element and see if it behaves like we expect". Its one of four standard feature detection techniques, [nicely summed up](http://diveintohtml5.info/detect.html) in Mark Pilgrim's [Dive Into HTML5](http://diveintohtml5.info/).

Knowing these patterns makes feature detection easier, but we can make it even easier than that. These days, we have library support too. The popular [Modernizr library](http://www.modernizr.com/) has your feature detection needs covered. Our canvas detection is as simple as `Modernizr.canvas`, so we can just include Modernizr and say:

    Modernizr.canvas ? showGraph() : showTable();

Feature detection is not just for scripts; thanks to [CSS Media Queries](https://developer.mozilla.org/En/CSS/Media_queries), the same principle applies to stylesheets too. For example, you could deliver a stripped-down appearance for devices with limited resolution:

    @media screen and (min-width: 400px) {
      header img, .sidebar { display: none; }
      p { margin: 0; }
    }

The new [matchMedia](http://peter.sh/2010/11/multiple-profiles-the-matchmedia-interface-and-locally-modified-files/) API is bringing such media queries into JavaScript.

## <span>Browser Detection</span>

Browser detection has fallen out of vogue, largely superceded by feature detection for reasons explained below, but is still necessary on occasion.

During the ["Browser Wars"](http://en.wikipedia.org/wiki/Browser_wars) of the 1990s, one of the key battlegrounds was developer features. Microsoft and Netscape constantly introduced new elements and capabilities. And so browser detection became commonplace. "Is this IE5? Great, then I'll use XMLHttpRequest; otherwise, I'll use an iFrame". This made some sense when IE5 was the only browser supporting XMLHttpRequest. Checking for IE5 is equivalent to checking for XMLHttpRequest directly, so many developers just did the IE5 check.

That, in a nutshell, is browser detection. "Are we running in (browser/version/OS)? Then do something specifically for (browser/version/OS)". Typically, it's used to ensure a certain feature exists, as in the XMLHttpRequest example above. It might also be used for user interface customization, for example "Is this Mobile Safari? Then I'll make the UI look like a native iOS app."

How do we perform browser detection? As with feature detection, there's no magic, only pragmatism and patterns. It also depends on what we mean by a browser: Do you want to know it's a member of the Opera family, or do you want to know it's Opera 9.0 running on Linux? Obviously, the more precise you get, the harder it is. Typically, we can determine browser by inspecting the `window.navigator` object - see [Peter-Paul Koch's browser detection library](http://www.quirksmode.org/js/detect.html) for more details. Browsers are also identified in the `User-Agent` request header, so it can also be determined server-side.

Time has not been kind to browser detection. First, the detection process is difficult and error-prone. It's not about Netscape Navigator 1 versus Internet Explorer 1 anymore; with so many browsers and versions out there, the `navigator` object alone could take on thousands of different values. So it's easy to make mistakes or exclude a lesser known browser altogether. Second, even if you could identify the browser, what are you going to do about it? Would you choose to use canvas conditional on the browser your app is running in? If so, you will have to research a long list of browsers and versions to discover which supports canvas. The list will inevitably contain errors and omissions, and you'll have the burden of keeping up with all the new browser versions appearing on a daily basis.

Browser detection does have a place in modern web develoment, but it's limited. One reasonable usage is when you care deeply about a particular platform, as in the iOS example earlier, where we deliver a custom UI for Mobile Safari. Feature detection won't help you in this situation. In this case, it's the environment itself that we care about, not its features. In the more extreme version, we might build an app purely for one browser (not a practice that will amuse everyone in the web standards community, but one that might make commercial sense). Another, very specific, situation where we need browser detection is for cross-browser research and testing. See [BrowserScope](http://browserscope.com), [HTML5Test](http://html5test.com), [TestSwarm](http://swarm.jquery.org/), and [JsPerf](http://jsperf.com).

Finally, there may be performance reasons to consider browser detection, too. Earlier this year, [Alex Russell](http://infrequently.org/), a Google Chrome engineer and a thought leader in the web development community, [began a conversation](http://infrequently.org/2011/01/cutting-the-interrogation-short/) which may cause the industry to take a more nuanced view on the feature-browser distinction. Alex suggests we can avoid the performance overhead of feature detection tests if we make use of existing knowledge about what works on various browsers. Furthermore, there is the argument that if we do this kind of thing server-side, we can ensure we only serve the code we need. No feature detection libraries and only the application code which browsers can make use of. As the reactions to Alex's post indicate, the jury is still out.

## <span>Form Factor Detection</span>

At Google IO 2011, Paul Kinlan and I introduced a new concept: form factor Detection. It's a new and largely untested idea, but we feel it's a necessary direction in light of the explosion of devices developers are struggling to support. HTML5 is clearly a step in the right direction, but we can't just deliver the same user experience to each environment; users have different needs and expectations. On the other hand, it's impractical for developers to customize their apps hundreds of times.

In short, we want to balance user experience with developer experience, and we argue there's a sweetspot here, which is a distinct user interface for each form factor. So we have a baseline app that runs everywhere, but a custom user-interface layer for all TV browsers, another for all desktop browsers, another for all smartphone browsers, and so on.

Form factor detection, in our view, maximizes code reuse while acknowledging that the different form factors need qualitatively different user experiences. It's not enough to just strip a few elements off your desktop app to make a mobile app; you really need to re-think what the app's all about in the mobile context, for example mobile apps are more prone to quick interactions than desktop apps. Meanwhile TV apps are more of a laid-back — sometimes ambient — experience.

As with the previous sections, we ought to look at the mechanics of form factor detection. How do we actually detect if we're running in a TV, versus a desktop, versus a mobile? Unlike the browser and feature, we unfortunately don't have much prior art here, so this is very much a research area. We would welcome a standard along these lines, where the browser would expose the form factor explicitly. But until that happens, we simply have to use a pragmatic mix of browser and feature detection. Yep, more detective work.

We released a proof-of-concept framework, [FormFactorJS](https://github.com/PaulKinlan/formfactor), which includes [indicator modules](https://github.com/PaulKinlan/formfactor/tree/master/indicators) for each form factor we care about. e.g. [the TV module](https://github.com/PaulKinlan/formfactor/blob/master/indicators/indicators.tv.js) makes use of a couple of known conventions for user agent strings inside TV browsers:

    formfactor.register({tv: [
    "tv",
    ( navigator.userAgent.indexOf("Large Screen") >= 0
       && navigator.userAgent.indexOf("GoogleTV/") >= 0 )
    ]});

Form factor detection is a useful complement to feature and browser detection. You can use it to structure your overall app architecture, with its various UI layers, and you can then tweak those UI layers further with feature and browser detection.

## <span>Summary</span>

Modern web development is no longer just about desktop browsers. Users work and play in a wide range of environments, and we can reach most of them with HTML5. As developers, we want to adapt our apps to each environment, ensuring great user experiences and making the most of whatever capabilities are available. The first step to environmental adaptation is environmental discovery, and that's what detection is all about.

Feature detection is the dominant type of detection on the web today, and for good reason. It aims to make a common app, with feature-dependent switches along the way depending on features, to accommodate for any possible combination of features offered by a particular browser.

Browser detection is no longer popular, because it was mostly used to determine if the current browser supported a particular feature — something better handled by feature detection. That said, there are still cases where developers want to raise the awesome level for a particular environment, and that's where browser detection shines.

Form factor detection is our intuition that it's important to build different UIs for smartphones versus desktops versus TVs, and so on. It's less important to differentiate between iPhone and Android (though you can still treat those as different form factors under this concept, should you want to customize even further).

Finally, it's worth emphasising the principle of progressive enhancement that is central to any form of detection. You will generally want to build a baseline app first, for a minimal browser. There's often a good case the app should even perform on a raw, non-JavaScript, browser like Lynx. Detection then becomes a way of augmenting this raw experience with more powerful functionality, dependent on the environment your app finds itself in. Remember the golden rule: We want our apps to be good for the environment, whatever the environment.