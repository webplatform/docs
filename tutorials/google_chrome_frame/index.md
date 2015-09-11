---
title: Rendering HTML5 in older browsers with Google Chrome Frame
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/google-chrome-frame/)'
readiness: 'Ready to Use'
summary: 'An introduction to rendering HTML5 in older browsers with Google Chrome Frame.'
tags:
  - Tutorials
  - Compatibility
uri: 'tutorials/google chrome frame'

---
**By [Malte Ubl](http://www.html5rocks.com/en/profiles/#malteubl)**

## <span>Summary</span>

An introduction to rendering HTML5 in older browsers with Google Chrome Frame.

## <span>Introduction</span>

HTML5 adds a multitude of new and awesome tools to the web developer toolbox, including:

-   New, more powerful JavaScript APIs
-   SVG for vector graphics
-   Canvas for 2D and with WebGL 3D graphics
-   CSS3 for rounded corners, gradients, etc.
-   More expressive markup

This list is, of course, not comprehensive; the web platform has moved forward massively, and the gap between old browsers and modern ones is widening every day. Every major desktop browser supports significant parts of HTML5, and increases its support with each new version. However, old browsers continue to linger and create a challenge for adopting the latest and greatest features today.

[Google Chrome Frame](http://www.google.com/chromeframe) can help you build state-of-the-art HTML5 pages while still allowing people using older browsers to see your content.

## <span>What is Google Chrome Frame?</span>

Google Chrome Frame is a plugin for Internet Explorer that enables rendering the full browser canvas using Google Chrome’s rendering engine. It seamlessly integrates all the HTML5 features supported by Chrome into the Internet Explorer user experience. Chrome Frame is available for Internet Explorer 6, 7, 8, and 9. Chrome Frame is certainly more useful when supporting old browser such as IE6 to IE8, but can be useful for IE9 users, as well.

Even if your site does not need HTML5 features, using Chrome Frame can still provide a better user experience. For example, page rendering is generally faster in Chrome Frame.

Alternatively, HTML5 polyfills provide another way to smooth out the transition to newer browsers. Unfortunately, they cannot emulate every feature, and they slow down your page in old browsers (which are already slower than the new generation) even more.

## <span>Opting in</span>

You can enable Chrome Frame to render a page by adding an HTML meta tag or using an HTTP header. By using one of these two methods, no site will break if a user has Chrome Frame installed, because the site is in full control of using the plugin or default rendering. The following two code snippets show how a site can opt into being rendered by Chrome Frame.

Option 1: HTTP-Header (you can add this to your [HTTP server (e.g., Apache) configuration)](http://www.chromium.org/developers/how-tos/chrome-frame-getting-started#TOC-Making-Your-Pages-Work-With-Google-):

    X-UA-Compatible: chrome=1

Option 2: Meta-tag (just paste this into your HTML \<head\> section)

    <meta http-equiv="X-UA-Compatible" content="chrome=1">

Once you have added either of these to your site, pages are rendered using Chrome Frame if it is installed on the user’s machine.

## <span>Prompting for Google Chrome Frame</span>

You may decide to fully deprecate support for old browsers for many reasons, such as:

-   Your site requires modern features such as HTML5 video, canvas, WebGL, or CSS3
-   Development time spent on old browsers is too high
-   Speed up development time for new features

Chrome Frame may provide a strategy to continue giving users of old browsers a way to still use your site, while continuing to enhance your site with HTML5 features.

Chrome Frame indicates that it is available by extending the host's User-Agent header with the string "chromeframe". For more information see [Chrome Frame User Agent](http://www.google.com/url?q=http%3A%2F%2Fwww.chromium.org%2Fdevelopers%2Fhow-tos%2Fchrome-frame-getting-started%2Funderstanding-chrome-frame-user-agent).

Use server-side detection to look for this token and determine whether Chrome Frame can be used for a page. If Chrome Frame is present, you can insert the required meta tag; if not, you can redirect users to a page that explains how to install Chrome Frame. As an alternative to server-side sniffing, you can use the CFInstall.js script to detect Chrome Frame and prompt users to install the plug-in without restarting their browsers. Using the script is straightforward; just add the script tags and optional styles to your page, as shown in the following example:

    <html>
    <body>
    <script type="text/javascript"
          src="http://ajax.googleapis.com/ajax/libs/chrome-frame/1/CFInstall.min.js">
    </script>

    <style>
       /*
       CSS rules to use for styling the overlay:
          .chromeFrameOverlayContent
          .chromeFrameOverlayContent iframe
          .chromeFrameOverlayCloseBar
          .chromeFrameOverlayUnderlay
       */
    </style>

    <script>
       // You may want to place these lines inside an onload handler
       CFInstall.check({
          mode: "overlay",
          destination: "http://www.waikiki.com"
       });
    </script>
    </body>
    </html>

Then, display a button to prompt users to install Chrome Frame:

    <button onclick="GCF_Install()">Install Chrome Frame
    (for IE only)</button>

### <span>Prompt yourself</span>

You may also decide to build a landing page or layer yourself. To do so:

-   Send users to this URL: <http://www.google.com/chromeframe/> which you can place in an IFRAME.
-   Append a redirect parameter to the URL to send users back to your site after installation is complete: <http://www.google.com/chromeframe/?redirect=http://www.google.com/>
-   Instead of going to the Chrome Frame landing page, you can also send the users directly to the EULA thus saving one step in the installation process: <http://www.google.com/chromeframe/eula.html>

### <span>No administrator rights needed</span>

To enable users to install Chrome Frame without having administrative privileges on their machines, append the `user=true` parameter to enable user level installation of Chrome Frame, as shown here:

    http://www.google.com/chromeframe/?user=true

### <span>Enterprise installation</span>

Enterprises can deploy Chrome Frame company-wide using the MSI installer which you can download here: <http://www.google.com/chromeframe/eula.html?msi=true>.

For more information on Chrome and enterprise deployments see <http://www.chromium.org/administrators>.

## <span>Adoption</span>

Many major websites such as [yahoo.com](http://yahoo.com), [wordpress.com](http://wordpress.com) and several Google properties have adopted Google Chrome Frame. Besides giving their users access to a more modern web experience for many sites, Chrome Frame also presents a significant improvement in initial load time. You can check whether Chrome Frame helps your site get faster rendering by going to [webpagetest.org](http://webpagetest.org) and selecting Chrome Frame as the browser.

## <span>More information</span>

For more information see the [Getting Started Guide](http://www.google.com/url?q=http%3A%2F%2Fwww.chromium.org%2Fdevelopers%2Fhow-tos%2Fchrome-frame-getting-started) or watch [this video](http://www.youtube.com/watch?feature=player_embedded&v=3YkEUpJQP3o) from Google IO 2011.