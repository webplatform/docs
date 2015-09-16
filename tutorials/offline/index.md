---
title: Offline apps
attributions:
  - 'Facebook HTML5 Resource Center.'
readiness: 'Ready to Use'
summary: "Mobile users expect to have the ability to open an app and interact with it, no matter if they have a connection.\n"
tags:
  - Tutorials
  - JavaScript
uri: tutorials/offline

---
## Summary

Mobile users expect to have the ability to open an app and interact with it, no matter if they have a connection.

AppCache provides a solution that allows you to cache your entire app on a user's device. This allows your app to continue working even when the user is offline. When the user is connected, AppCache will also make the app load faster by minimizing the number of requests made to your server.

In addition to the benefits offered by AppCache, modern browsers allow storing of a user's app specific data, for example their high scores in a game, via localStorage. Using these two features enables your app to work in an offline state.

Gmail, for example, uses both of these features so that you can continue to read your emails, even on a plane.

Note that this guide focuses on mobile, but the same practices can be applied to desktop, as well.

## Caching the App

[App Cache](http://www.whatwg.org/specs/web-apps/current-work/#applicationcache) allows caching of static resources like images, CSS, and Javascript. Using AppCache, these resources only need to be requested the first time the app is run, or whenever it is updated. AppCache is currently supported on Chrome 10.0+, Firefox 3.6+, IE 10.0, Opera 10.6+, Safari 4.0+ and on iPhone 2.1+, Android 2.0+. For up-to-date compatibility support, check out [CanIUse.com's support table](http://www.caniuse.com/#search=appcache).

You can enable AppCache by including a simple text file, called a cache manifest, that specifies which resources should be preloaded and cached for offline access. All HTML pages should reference this manifest file by including the `manifest` attribute in the html tag. Here's an example.

    <html manifest="myapp.appcache">
      ...
      ...
    </html>

Note that any page that references the cache manifest will be cached by the browser and need not be included in the manifest file. The manifest file must be served from the same domain as the app and must have a `text/cache-manifest` MIME type. For example, to serve this mime-type in Apache, add this line to the `.htaccess` file, which will serve a `text/cache-manifest` MIME type for files with an `.appcache` extension:

    AddType text/cache-manifest .appcache

### Structure of a Manifest File

A simple manifest file looks like this.

    CACHE MANIFEST
    fbstyle.css
    js/graph_api.js
    js/auth.js
    res/facebook.png
    res/places.png

In this particular example, all five resources listed, along with HTML page that referenced the manifest, and the manifest file itself, will be cached. Note that the entire cache process fails if one of the specified resources cannot be loaded. As of today, most implementations limit the size of the cached data to 5MB per domain.

The manifest file does offer more granular controls such as listing alternate resources in case of failures and listing files which require network access. Let's look at more complex example.

    CACHE MANIFEST
    # Update revision number to trigger a cache refresh
    # v0.4.3-11-fac3b00c

    # Should always be cached
    CACHE:
    fbstyle.css
    js/graph_api.js
    js/auth.js
    img/facebook.png
    img/places.png

    # User must be online for these actions:
    NETWORK:
    auth.php
    logout.php
    checkin.php

    # serve offline.png if fails to get images in img folder
    # serve offline.html if fails to get index.html
    FALLBACK:
    img/ images/offline.png
    index.html /offline.html

A manifest can have three distinct sections, which can be listed in any order and can also appear more than once:

`CACHE`: the default section for entries. Files listed under this section (or immediately after the CACHE MANIFEST) will be explicitly cached after they're downloaded for the first time.

`NETWORK`: resources listed under this section require network access. By default, AppCache won't allow network access to files which aren't specified in this section. Thankfully, you can override this default behavior by using the online whitelist wildcard flag (the asterisk '\*') which allows any external content to be accessed directly. For example, the below manifest file would cache `app.css`, `app.js`, and `img/logo.png` but would allow direct access to any other file the app might require:

    CACHE MANIFEST
    app.css
    app.js
    img/logo.png

    NETWORK:
    *

You can also use prefix match patterns if you want tighter control. For example, the following manifest file would allow network access to all files in the `img/` and videos/ directories, but wouldn't display resources stored elsewhere.

    CACHE MANIFEST
    app.css
    app.js

    NETWORK:
    img/
    video/


`FALLBACK`: specify a fallback for uncached resources when there is no network connection. Obviously, the fallback resource itself will be cached. Like the `NETWORK` section, `FALLBACK` lets you use prefix match patterns. This could be used, for example, to provide a fallback page for all archived content:

    CACHE MANIFEST
    # ...
    FALLBACK:
    archives/ offline.html

### Updating the Cache

Updating the cache is a bit more involved. Whenever your app is loaded, if your app calls the `window.applicationCache.update()` API, or if the user wiped out its cache, AppCache will attempt to download the manifest file again and check to see if there have been changes to it. If the server responds with a `304 Not Modified` header or if the downloaded manifest file is byte-for-byte equivalent to the previous one, nothing happens. On the other hand, if there are changes, AppCache will download all resources again. To avoid generating extra traffic, it will use its previous cache as if it were a local HTTP cache, and, in doing so, will conform to any HTTP directives you might have set.

To make sure changes to your manifest file are correctly picked up by AppCache, you will want to make sure that it doesn't get cached by the browser's HTTP cache. If you're using Apache, this is done by adding the following directives to your `.htaccess` file:

    ExpiresActive On
    ExpiresByType text/cache-manifest "access"

You also need to keep in mind that only modifications to the manifest file itself will trigger a cache refresh. Just modifying a resource won't. You'll have to either rename the modified asset (and update the manifest file accordingly) or include a version number, revision number or timestamp in a comment in the manifest file like so:

    CACHE MANIFEST
    # Update revision number to trigger a cache refresh
    # v0.4.3-12-1337fac3

### JavaScript API

AppCache's [JS API](http://dev.w3.org/html5/spec/offline.html#application-cache-api) is currently limited but can still prove useful for debugging purposes (see Jonathan Stark's [script](http://jonathanstark.com/blog/2009/09/27/debugging-html-5-offline-application-cache/)), force swaps on long-lived apps or to prompt users to refresh their app once it has been updated.

Prompting the user when a new version of the app has been downloaded can be done as follows:

    var appCache = window.applicationCache;
    appCache.addEventListener('updateready', function(e) {
      if (appCache.status == appCache.UPDATEREADY) {
        // The new cache has been downloaded. Prompt the user
        // to see if he wants to refresh his page now.

        var msg = 'A new version of the app has been downloaded.\n'
        msg += 'Click OK to use it now or Cancel to continue using the current version.'

        if (window.prompt(msg)) {
          window.location.reload();
        }
      }
    }, false);


On long-lived apps, you'll have to add a timer that regularly checks the manifest file for changes. When changes are detected, an `updateready` event will also be triggered, calling the event handler and prompting the user:

    window.setTimeInterval(function() {
      appCache.update();
    }, 1000 * 60 * 60 * 24); // Checks for updates once a day.

## Caching Dynamic Content

Web apps may want to locally store dynamic user generated content like email or a game's scoreboard. Currently, cookies have been used to work around this shortcoming and offer local storage, but cookies are limited by data size. Cookies are also included in every http request which not only slows down your app but also potentially exposes security risks.

HTML5 overcomes these restrictions by offering local data storage options, which persist over page refresh and browser exit, and are not transmitted over the network. HTML5 storage is implemented natively in the browser, without the need for a plugin, and stores the data in key/value pairs.

HTML5 storage is supported by almost all browsers: Chrome 10.0+, Firefox 3.6+, IE 8.0+, Opera 10.6+, Safari 4.0+ and on iPhone 2.0+, Android 2.1+. For up-to-date compatibility support, check out [CanIUse.com's Local Storage support table](http://www.caniuse.com/#search=storage).

### Detecting HTML5 Storage support

You can use Modernizr to detect support HTML5 Storage:

    if (Modernizr.localstorage) {
      // HTML5 Storage is supported
    } else {
      // HTML5 storage not supported
      // try PersistJS or a third-party solution
    }

### Storing the content

HTML5 stores data in key/value pairs. Note that both key and values are coerced to strings, so you might need to revive your data back to its original type when accessing it.

    // Store data, this overwrite any previous value for "One" key
    localStorage.setItem("one", 1);

    // Retrieve data
    var one = parseInt(localStorage.getItem("one");

    // or using square brackets:

    localStorage["one"] = 1;
    var one = parsetInt(localStorage["one"]);

    // or even:

    localStorage.one = 1;
    var one = parsetInt(localStorage.one);

    // Delete the key's value, do nothing if key does not exist.
    localStorage.removeItem("one");

    // Clear the entire storage. Note that this wipes out everything, worth noting
    // if more than one person working on the same app is relying on localStorage.
    localStorage.clear();

A common and useful technique to store structured data is to use JSON:

    var obj = { foo: { bar: 123 } };
    localStorage.someObj = JSON.stringify(obj);

    // later on:

    var obj = JSON.parse(localStorage.someObj);
    obj.foo.bar; // => 123

### Listening to Changes to the Storage

You can register listeners for `setItem()`, `removeItem()`, `clear()` functions, which will be called when the data in the storage changes.

    if (window.addEventListener) {
      window.addEventListener("storage", storage_listener, false);
    } else {
      window.attachEvent("onstorage", storage_listener);
    }

The `storage_listener` function will be called with a `StorageEvent` object:

|Property|Type|Description|
|:-------|:---|:----------|
|key|string|The key that was changed, added or removed.|
|oldValue|any|The old value of the changed key or null if new key.|
|newValue|any|The new value of the added/changed key or null if removed.|
|url|string|The url that triggered the change.|

### Potential Pitfalls

Local Storage has a single data store for each domain: e.g. there's a single instance of `localStorage` for <http://www.example.com>. The data it contains is shared across sessions and is not encrypted. While this is possibly fine on mobile, it could be an issue on shared computers. The data contained in `localStorage` is available to anyone who visits <http://www.example.com>, whether or not the user is logged in or is the previously logged in user.

### Data Storage Limits

Most implementations have a 5MB storage limit. More storage is often available, but the user will be prompted for it. Expect a `QUOTA_EXCEEDED_ERR` or similar error if the limit is exceeded or if the user refuses to allocate more storage for your app.

### Libraries and Demos

-   [PersistJS: Cross Browser Client-Side Persistent Storage Without Cookies](http://pablotron.org/?cid=1557)
-   [PersistJS source code](https://github.com/jeremydurham/persist-js)
-   [Kindle Cloud Reader](https://read.amazon.com)
-   [TrappistDB: demo of cross-browser persistant data storage](http://futtta.be/NoWebDB/)

## Additional Resources {\#resources}

-   [A Beginner's Guide to Using the App Cache](http://www.html5rocks.com/en/tutorials/appcache/beginner/)
-   [Dive into HTML5 Offline](http://diveintohtml5.org/offline.html) - caching the static resources for web apps
-   [Dive into HTML5 Local Storage](http://diveintohtml5.org/storage.html) - persistent local storage for web apps
