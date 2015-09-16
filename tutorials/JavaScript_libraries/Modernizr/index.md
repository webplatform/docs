---
title: 'Modernizr'
notes:
  - 'Should not be a webplatform.org topic; deletion candidate'
readiness: 'Not Ready'
summary: 'Modernizr is a JavaScript library that detects HTML5 and CSS3 features in the user’s browser.'
tags:
  - Tutorials
  - JavaScript
  - Library
uri: 'tutorials/JavaScript libraries/Modernizr'

---
**By [Avinash Zala](http://www.xpertdeveloper.com)**

## Summary

Modernizr is a JavaScript library that detects HTML5 and CSS3 features in the user’s browser.

## Why use Modernizr?

As web grows we are getting something new every day. And obviously all new features are not supported in all browsers. But some browsers like Chrome, Safari keeps updating as per the new features. So what about the browsers which don't support new features (e.g. IE7 for HTML5). Here Modernizr comes into picture. Modernizr is used to detect the browser support of any HTML5 feature.

## How it Works?

Modernizr runs on page load to detect the support of HTML5 and CSS3 features in the current browser; after that it creates a JavaScript object with the results, and adds classes to the `html` element for you to key your CSS on.

## Key Facts

-   It tests for over 150 next-generation features, all in a matter of milliseconds
-   It creates a JavaScript object (named Modernizr) that contains the results of these tests as boolean properties
-   It adds classes to the html element that explain precisely what features are and are not natively supported
-   It provides a script loader so you can pull in polyfills to backfill functionality in old browsers

## Install Modernizr

To install Modernizr, download a copy from [modernizr.com](http://modernizr.com/). You can choose the Development version which includes the 40+ core tests, or [build a custom download](http://modernizr.com/download/) by picking only the features you want from the 150+ available.

Next, you simply include the library in the `head` of your HTML page, like so:

    <script src="path/to/modernizr.js"></script>

The library will run automatically when the page loads, and make the results available to you via classes on the `html` element, and as properties on a global `Modernizr` JavaScript object, for example:

    Modernizr.video; // true or false, depending on the browser's support for HTML5 video

## Notes

There are some features that Modernizr cannot detect. See [The Undetectables](https://github.com/Modernizr/Modernizr/wiki/Undetectables) on Modernizr’s wiki for more information.

Other features may yield what are known as *false positive* results in some browsers: the browser claims to support a feature, but its support is actually missing, broken or incomplete. Modernizr does its best to detect these false positives and will make exceptions for those cases, to offer you the most accurate feature detection available.
