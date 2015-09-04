---
title: libraries
tags:
  - Basic
  - Pages
  - JavaScript
readiness: 'Not Ready'
summary: 'Introduction to JavaScript libraries'
uri: concepts/programming/javascript/libraries

---
# JavaScript libraries

## Summary

Introduction to JavaScript libraries

**Merge Candidate**: This page is a candidate for merge with the following pages: [[[1]](http://docs.webplatform.org/wiki/javascript/libraries)]

## Overview

JavaScript is arguably the most widely used computer language in the world. The use cases where JavaScript has shown to be replacing traditional platforms are ever increasing. As the scope of the usage grows, it becomes extremely important that a method of distribution of code is used, to not only bring simplicity in further development but also allow reuse of code by the masses. JavaScript libraries solve this problem really well, and there are dozens if not hundreds of libraries available that cater to various use cases.

These various libraries provide pre-written JavaScript code which makes common or complex tasks easy to do. JavaScript libraries often target specific tasks such as DOM manipulation, framework setup and AJAX handling.

## Benefits

-   **Uniform interface for cross-browser compatible code** - While modern browsers are becoming increasingly similar in their implementations of the language features and DOM, numerous minor differences still exist. The problem becomes substantial when compatibility with older browsers is required. Quite a few JavaScript libraries try to reduce the boilerplate code that developers have to write to address this issue. They provide a uniform API for development, which all compatibility handling throw browser and feature detection is handled in the background.

-   **Higher levels of abstraction** - Quite often it is the case that development requires implementations of features that are quite popular in the industry. Auto-completion, AJAX handling, graphics and user interface elements are some examples of areas where libraries can be a big boon. Most efforts can then be focused on customization.

-   **Frameworks** - While the language itself is quite powerful and yet extremely easy to use, developing and maintaining large code bases can become challenging. There are various frameworks available as JavaScript libraries that implement designs like MVC for writing the code in a more structured fashion.

## Getting started

The most commonly used libraries have rich communities and forums where you can find help to get started with that particular library. JavaScript libraries are often downloaded from the library developer site. Many library developers provide both development and production versions of their libraries. The development versions contain non-minified code which often include comments and hints whereas the production versions often are minified and compressed for live site use.

Optionally, many libraries are available from [content delivery networks (CDN)](http://en.wikipedia.org/wiki/Content_delivery_network) such as [cdnjs](http://cdnjs.com/), [Google Hosted Libraries](https://developers.google.com/speed/libraries), [jsDelivr](http://jsdelivr.com/) and [Microsoft Ajax Content Delivery Network](http://www.asp.net/ajaxlibrary/cdn.ashx). You can find more of these and comparisons between them at [cdnperf](http://www.cdnperf.com).

### Usage

To include a library in your application you simply add a `<script>` element to your `<head>` element with the `src` attribute referencing the URL or path to the library's source. Below, you see two examples on how to load the jQuery library, one from jsDelivr and one from a local path.

#### Examples

From CDN (jsDelivr):

``` {.html}
<script src="//cdn.jsdelivr.net/jquery/2.1.3/jquery.min.js"></script>
```

 From a local path:

``` {.html}
<script src="js/lib/jquery.min.js"></script>
```

## Common libraries

This list showcases JavaScript libraries. They're sorted alphabetically. If you don't see yours, please add it to the list.

Library
:   Type
[ajile](http://ajile.net)
:   Modules
[AngularJS](http://angularjs.org)
:   Framework
[Backbone](http://backbonejs.org/)
:   Framework
[FabricJS](http://fabricjs.com)
:   Graphics
[EaselJS](http://createjs.com/EaselJS)
:   Graphics
[EmberJS](http://emberjs.com)
:   Framework
[Ext JS](http://sencha.com/products/extjs/)
:   Framework
[GLGE](http://www.glge.org/)
:   Graphics
[jQuery](http://jquery.com)
:   Tools and Utilites
[Meteor](http://meteor.com/)
:   Complete Stack
[Prototype](http://prototypejs.org/)
:   Framework & Utilities
[Raphaël](http://raphaeljs.com/)
:   Vector Graphics
[SproutCore](http://sproutcore.com/)
:   Framework
[Underscore](http://underscorejs.org/)
:   Framework
[YUI Library](http://yuilibrary.com/)
:   JS/CSS Framework

