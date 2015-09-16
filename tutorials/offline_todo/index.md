---
title: Taking your to-do list offline
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/offline/takingappoffline/)'
notes:
  - 'Links point to HTML5Rocks! that should point to internal copies.'
readiness: 'Almost Ready'
summary: 'A guide to taking web apps offline.'
tags:
  - Tutorials
  - Appcache
uri: 'tutorials/offline todo'

---
**By Paul Kinlan**
Originally published published June 18, 2010, updated Sept. 4, 2012

## Summary

A guide to taking web apps offline.

## Introduction

There are two main components to Offline support in HTML.

-   The Application Cache, used for caching application files such as HTML, images, JavaScript and CSS
-   Databases, used for data access and key-based lookups such as localStorage and sessionStorage

This sample demonstrates how to take your applications offline using the Application Cache, by extending the Database functionality in the HTML5Rocks! [to-do list manager](http://www.html5rocks.com/en/tutorials/webdatabase/todo/) tutorial.

The TODO list manager already demonstrates the use of client-side databases, so combining this with the Application Cache and using all the same Javascript and HTML will give you a clear indication of how simple it can be to take your applications offline.

## What is the Application Cache?

The Application Cache (App Cache for short) is designed to let you declaratively specify your web application's required resources in a manifest file. The resources listed in the manifest will be proactively downloaded and stored by the browser.

## Step 1. Creating a basic manifest

Because we already have an application on the web, it is a simple process to add offline support. The first thing we need to do is to create our manifest file.

     CACHE MANIFEST
     # Revision: 1
     index.html
     script.js
     base.css

The manifest file contains a comment (the line beginning with "\#") and a list of the three files that we will be using.

The browser will re-download all the files in the manifest if it detects any change in the manifest file. Therefore, if you are deploying software and making changes, you can use the comment line to ensure that all your users download the latest application.

## Step 2. Attaching the manifest

For the browser to be able find the manifest file, we need to reference it from the root `<html>` element.

     <html manifest="cache.manifest">

The presence of this attribute instructs the browser to download the manifest file and start the process of acquiring the resources needed to ensure your application is available in offline mode.

## Step 3. Pulling the plug (Testing)

If you have correctly listed all the application files, then your application will be available offline.

For an example, see our sample application at HTML5Rocks!: [Offline To-do list](http://www.html5rocks.com/en/tutorials/offline/takingappoffline/todo/sample.html). In this application, we are using all the same code as our previous To-do sample, but now it is available offline.

## Taking it further

This is a pretty simple example; in reality, applications are a little more in-depth. So now is a good time to cover some more features of the App Cache.

### Mixing offline and online

Quite often you will not want to package all your files inside one offline manifest. For instance, you might have an online help system that your users will reference.

To ensure that your users don't get a "404 Page Not Found" error when visiting your help pages, you can specify a "FALLBACK" page in your manifest. This page will be presented to your users in place of the default 404 page.

     CACHE MANIFEST
     # A list of the files that are need for this application
     # Rev 25
     index.html
     script.js
     base.css

     FALLBACK:
     / offline.html

To see this in action use our sample HTML5Rocks! [Offline To-do list](http://www.html5rocks.com/en/tutorials/offline/takingappoffline/todo/sample.html) application, disconnect from the Internet, and then and click on [Online help](http://www.html5rocks.com/en/tutorials/offline/takingappoffline/todo/help.html). You should see a Whoopsie page.

### Accessing dynamic content

By default, the application cache will not allow users to access resources that have not been defined in the manifest. This means that access to dynamic data, such as a back-end database or a remote web API such as Twitter, will fail.

The designers of the spec anticipated this scenario and created a "NETWORK" section in the manifest definition that allows you to specify a whitelist of addresses that will always be allowed through the cache.

     CACHE MANIFEST
     # A list of the files that are need for this application
     # Rev 26
     index.html
     script.js
     base.css

     NETWORK:
     /getweather

In this example, any requests to our "/getweather" API will be allowed through.

If we had another API called "/getstocks", but it wasn't defined in the "NETWORK" section, all requests to that API would fail.

But let's say you have too many APIs or remote resources to enumerate in the manifest file; what can you do? The designers thought of this too and allow you to white-list those resources.

     CACHE MANIFEST
     # A list of the files that are need for this application
     # Rev 26
     index.html
     script.js
     base.css

     NETWORK:
     bin/*

You can now call any resource in the bin directory.

When your application goes offline, requests to anything in the "NETWORK" section will fail and will need to be handled by your code. The FALLBACK mechanism will not kick in.

### Detecting updates

There is a very strong chance that you will need to update your application, whether to fix bugs or to add new functionality. Once an application is offline, it remains so until users clears their browse cache or until you programatically update their version of the code.

The good thing is, the browser can handle all of this. Earlier we talked about the browser detecting updates to the manifest. When this occurs the browser will download all the latest resources and send an event to your JavaScript indicating that an update is available. You can present your users with a notification to inform them that they can update the application to the latest version.

     // Called onload of the body element
     init = function() {
       var status = document.getElementById("#status");
       var updateButton = document.getElementById("#update");
       updateButton.addEventListener("click", updateApplication);

       window.applicationCache.addEventListener('updateready', function() {
         status.innerText = "There is an update ready";
         }, false);
     };

     updateApplication = function(){
       // Ensure the browser uses the latest version of the code
       window.applicationCache.swapCache();
       // Reload the application
       window.location.reload();
     };

Note that some browsers will load the new application the next time your user uses your application. Some browsers will require you to perform a swapCache(), therefore it makes sense to programatically update the user to the new version.

### Accessing web APIs

Let's say you are building a Google Buzz client. You have made it offline-enabled and you want to use JSONP to access Buzz directly. You will quickly find that it won't work. App Cache doesn't let you white-list requests to cross-domain resources.

So what can you do? You will need to build a simple proxy on your domain that you can use to white-list requests to external resources.

## Wrapping it up

We have seen that it is pretty simple to take your existing applications offline. At the simplest level it is just a process of defining a basic manifest file and attaching it to your root `<html>` element.

We have also seen the extra things that you can do to drastically improve the user experience of your applications with enhancements such as NETWORK whitelisting, FALLBACK support, and capturing events.

But the best thing of all is, your application will still work online with browsers that don't support App Cache.
