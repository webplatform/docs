---
title: building web apps
tags:
  - Tutorials
  - Developer
  - Tools
  - HTML
  - JavaScript
readiness: 'Ready to Use'
summary: 'In this tutorial, we''ll provide you with the architectural understanding, frameworks and tools you''ll need in order to create web apps.  We''ll also explain how they should be used and how they fit together.'
uri: 'tutorials/building web apps'

---
# Building web apps

## Summary

In this tutorial, we'll provide you with the architectural understanding, frameworks and tools you'll need in order to create web apps. We'll also explain how they should be used and how they fit together.

## Architecture

First, think of this simple use case. A user lands on a mobile web app that displays movie listings and clicks on a link to the "Inception" movie.

![web app flow 1.png](/assets/public/5/5d/web_app_flow_1.png)

This is how a traditional website would handle the user experience, using redirects.

![web app flow 2.png](/assets/public/c/c5/web_app_flow_2.png)

First, the user lands on the movie listing website. The web server sends back all of the markup (HTML, CSS), JavaScript and data in order to display the page. Next, the user clicks on the "Inception" movie. The browser is then redirected to `/movies/inception`.

Again, the server sends back all of the markup, JavaScript and data in order to display the page. It can often be a jarring user experience because you cannot control the visual flow of the last content disappearing and the new content appearing. It's also likely this is much slower than it has to be, since there’s a lot of unnecessary data being exchanged.

Now consider the same user scenario, but with the "web app" design paradigm. This flow prevents unnecessary redirects and thus feels faster and smoother to the user.

![web app flow 3.png](/assets/public/6/60/web_app_flow_3.png)

First, the user lands on the movie listing website. The web server sends back static resources like HTML, JavaScript, CSS and images. Think of this as the equivalent resources that you would have in a compiled native app. These resources contain everything the web app needs to function, but it doesn’t include any dynamic data (like movie listings).

Once the browser has downloaded the static resources, it then fires an AJAX request for the API method `getMovies`. This tells the server that the browser is asking for movie listings. It then passes back only the JSON-encoded data that’s needed to show the listings, for example:

    {
        "movies": [
            {"id": 34, "title": "Inception", "year": 2010},
            {"id": 47, "title": "The Social Network", "year": 2010}
        ]
    }

Once the browser receives this data, the JavaScript, HTML and CSS that was initially downloaded interprets the data and displays the movie listings page.

Then, the user clicks on "Inception" and the browser sends another AJAX request for this data to `/api?method=getMovie&id=34`. The server returns only the data needed to display the Inception movie page, for example:

    {
        "title": "Inception",
        "picture": "inception.jpg",
        "cast": [
            "Leonardo Dicaprio",
            "Ellen Page"
        ]
    }

Again, once the browser receives this data, the JavaScript, HTML and CSS that was initially downloaded interprets the data and displays the Inception movie page.

In this flow, the user never navigates away from the first page they land on. Because of that, you can think of a web app as a "single-page website", as opposed to the traditional "multiple-page website".

## Building JSON APIs

For more information on building proper JSON APIs, [check out this excellent guide](http://bitworking.org/news/restful_json).

Also, note that WebSockets is a newly available technology that allows real-time communication between the browser and your server. This is useful for building web apps like a chat client. For more information, see [the tutorial on HTML5 Rocks](http://www.html5rocks.com/en/tutorials/websockets/basics/) or check out [the docs on the Mozilla Developer Network](https://developer.mozilla.org/en/WebSockets). Note that support is limited, though.

Now that you have an overview of what a web app is, and you have some background on building APIs, let’s start building the web app client.

## MVC Frameworks

Using a Model-View-Controller (MVC) model will help you make your JavaScript code more flexible and easier to maintain. This is especially important since you’re building a web app, which will likely be handling complicated data. MVC is a design pattern that breaks a web app into three parts: the data (Model), the presentation of that data to the user (View), and the actions taken for any user interaction (Controller).

We’re not going to dive too deeply into this subject since there are great resources already available. For an excellent primer to understand how MVC works in JavaScript, see [the article on A List Apart](http://www.alistapart.com/articles/javascript-mvc/).

There are a lot of very popular JavaScript frameworks already available, but very few of them use a MVC model. However, there are a couple of burgeoning open source frameworks available.

### Backbone JS

Backbone JS is a lightweight MVC framework that features key-value binding, custom events,and views with declarative event handling. Typically, developers write the UI themselves or pair Backbone with other JavaScript frameworks like jQuery or Zepto (more on those below).

You can read more about it on the [Backbone JS website](http://documentcloud.github.com/backbone/), or you can check out the [Backbone Fundamentals book](https://github.com/addyosmani/backbone-fundamentals).

Example web apps that use Backbone include [SoundCloud](http://m.soundcloud.com/), [Basecamp](http://basecamphq.com/mobile) and [Pandora](http://www.pandora.com/newpandora).

### Ember.js

Ember.js is an MVC framework focused on data-centric apps. It provides a data-binding system that ensures that changes to data propagate correctly across all of the views of your web app. It also provides a standard application architecture, with built-in support for state management.

You can read more about it on [Ember's website](http://www.emberjs.com/).

A number of live web apps are actively using Ember, including [Square](https://squareup.com/), [Zendesk](http://www.zendesk.com/) and [LivingSocial](http://livingsocial.com/).

## Other Frameworks

The landscape of JavaScript frameworks is constantly changing; we've profiled Backbone and Ember, but there are many other frameworks to choose from, some of which [are compared here](http://codebrief.com/2012/01/the-top-10-javascript-mvc-frameworks-reviewed/).

If you're having trouble deciding which framework to use, you should check out [TodoMVC](http://addyosmani.github.com/todomvc/). It gives example code for the same Todos app written using several different frameworks; you can compare the syntax and performance to choose what makes most sense for your app.

If you’re not interested in maintaining an MVC model, we recommend these frameworks:

### jQuery

jQuery exposes a rich set of functions for traversing and manipulating your web app.

However, jQuery doesn’t employ a MVC model. Many developers couple it with Backbone.js to get the benefit of MVC while also getting jQuery functionality to interact with UI (e.g. traversing and manipulating the document, and animating).

You can read more about it on [jQuery's website](http://www.jQuery.com/).

Many websites use jQuery, including [Technorati](http://www.technorati.com/), [CBS](http://www.cbs.com/) and [MLB](http://www.mlb.com/).

## Mobile Frameworks

Mobile frameworks are specifically smaller than most frameworks so that they load fast. They may also contain mobile browser-specific functionality or workarounds.

### Zepto

Zepto is specifically built to run on mobile WebKit browsers. It’s a very small library meant to handle a lot of commonly used functionality that’s available in other frameworks like jQuery, including event chaining and document traversal and manipulation.

Zepto has been adopted by a handful of mobile web apps, including [Basecamp](http://basecamphq.com/mobile) and [Linkedin](http://blog.linkedin.com/category/linkedin-mobile/).

### jQuery Mobile

jQuery Mobile is built with a "commitment to universal accessibility" in mind; it supports [most platforms](http://jquerymobile.com/demos/1.1.0/docs/about/platforms.html) and provides easy theming for your app. It is designed to be easy to learn, especially for those already familiar with jQuery.

jQuery Mobile has a great [resource center](http://jquerymobile.com/resources/) with tutorials, tools, and examples to help you get started.

Many mobile sites are using jQuery Mobile, including [Slideshare](http://www.slideshare.net/mobile), [OpenTable](http://m.opentable.com/), and [Box](https://m.box.com/).

### Sencha Touch

Like Zepto, Sencha Touch targets mobile WebKit browsers. It provides a large set of UI features aimed at helping web apps feel more native, with fast animations and smooth scrolling.

You can read more about it on [Sencha's website](http://www.sencha.com/products/touch/).

A handful of apps are running on Sencha, including [Kiva Touch](http://www.sencha.com/apps/kivatouch/) and [O'Reilly Conferences](http://www.sencha.com/apps/oreilly-conferences-app/).

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Facebook HTML5 Resource Center.

