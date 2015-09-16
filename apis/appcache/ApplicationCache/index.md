---
title: ApplicationCache
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Using_the_application_cache)'
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The Application Cache (AppCache) lets web-based applications run offline. Developers can specify resources for the browser to cache, making them available to the application even if no connection can be made to the server. These resources load and work correctly even if users click the refresh button when they are offline.'
tags:
  - API
  - Objects
  - Appcache
uri: apis/appcache/ApplicationCache

---
## Summary

The Application Cache (AppCache) lets web-based applications run offline. Developers can specify resources for the browser to cache, making them available to the application even if no connection can be made to the server. These resources load and work correctly even if users click the refresh button when they are offline.

## Overview

An application cache provides the following benefits:

-   Offline browsing: users can navigate a site or use a web application although they are offline
-   Speed: cached resources are local, and therefore load faster
-   Reduced server load: the browser only downloads resources that have changed from the server.

## Properties

API Name
:   Summary

[oncached](/apis/appcache/ApplicationCache/oncached)
:   The resources listed in the manifest have been downloaded, and the application is now cached.

[onchecking](/apis/appcache/ApplicationCache/onchecking)
:   The user agent is checking for an update, or attempting to download the manifest for the first time. This is always the first event in the sequence.

[ondownloading](/apis/appcache/ApplicationCache/ondownloading)
:   The user agent has found an update and is fetching it, or is downloading the resources listed by the manifest for the first time.

[onerror](/apis/appcache/ApplicationCache/onerror)
:   Indicates an error has occurred.

[onnoupdate](/apis/appcache/ApplicationCache/onnoupdate)
:   Indicates the manifest has not changed.

[onobsolete](/apis/appcache/ApplicationCache/onobsolete)
:   The Webpage is associated with an application cache whose group is marked as obsolete.

[onprogress](/apis/appcache/ApplicationCache/onprogress)
:   The user agent is downloading resources listed by the manifest. The event object's total attribute returns the total number of files to be downloaded. The event object's loaded attribute returns the number of files processed so far.

[onupdateready](/apis/appcache/ApplicationCache/onupdateready)
:   The ApplicationCache object's cache host is associated with an application cache whose application cache group's update status is idle, and whose application cache group is not marked as obsolete, but that application cache is not the newest cache in its group.

[status](/apis/appcache/ApplicationCache/status)
:   Returns the current status of the application cache, as given by the constants defined below.

## Methods

API Name
:   Summary

[abort](/apis/appcache/ApplicationCache/abort)
:   Cancels the application cache download process. This method is intended to be used by Web applications showing their own caching progress UI, in case the user wants to stop the update (e.g., because bandwidth is limited).

[swapCache](/apis/appcache/ApplicationCache/swapCache)
:   Switches to the most recent application cache, if there is a newer one. If there isn't, throws an **InvalidStateError** exception.

    This does not cause previously-loaded resources to be reloaded; for example, images do not suddenly get reloaded and style sheets and scripts do not get reparsed or reevaluated. The only change is that subsequent requests for cached resources will obtain the newer copies.

    The **updateready** event will fire before this method can be called. Once it fires, the Web application can, at its leisure, call this method to switch the underlying cache to the one with the more recent updates. To make proper use of this, applications have to be able to bring the new features into play; for example, reloading scripts to enable new features. An easier alternative to `swapCache()` is just to reload the entire page at a time suitable for the user, using `location.reload()`.

[update](/apis/appcache/ApplicationCache/update)
:   Invokes the application cache download process. Throws an InvalidStateError exception if there is no application cache to update. Calling this method is not usually necessary, as user agents will generally take care of updating application caches automatically. The method can be useful in situations such as long-lived applications. For example, a Web mail application might stay open in a browser tab for weeks at a time. Such an application could want to test for updates each day.

## Events

*No events.*

## Usage

     In order to cache files, you must do the following:

-   Create a manifest file that lists the files and other web resources you want to cache.
-   Reference the manifest file in the header of every page you want cached.

### The manifest file

The manifest file defines which web resources are cached when a user browses to your site. The manifest file typically has the extension **.appcache** or **.manifest**. Each webpage must add a manifest attribute to the HTML element similar to this:

    <html manifest="example.appcache">

You can use an absolute or relative URL. The cache manifest file lists the files that will be cached, using the format:

    CACHE MANIFEST
    # Version 1

    CACHE:
    script/scriptfilename1.js
    css/cssfilename.css
    images/imagename1.png
    images/imagename2.jpg
    images/imagename3.png

    FALLBACK:
    # This will enable imagename4.png to be as a replacement for
    # all resources under the images dir when there is no network connectivity.
    images/ images/imagename4.png

    NETWORK:
    # This will prevent other network resources from being accessed.
    images/imagename5.png

The first line of the manifest must read CACHE MANIFEST and the lines that follow it list the web resources you want to cache. You can use the \# symbol to make comments.

Alternatively, web resources that need to be cached can be specified by adding a “CACHE:” header section before the resources (as shown previously). In addition, fallback resources can be defined to replace general or specific web resources when there is no network connectivity. This is done by adding a “FALLBACK:” header section before the resources. These resources can be wildcard to specify a catch all mechanism (as shown previously). Be aware that there is a space after the first "images/" in the FALLBACK: section. This indicates that any files contained under the "images/" directory will fall back to a specific web resource (for example, images/imagename4.png) if they cannot be accessed from the network. Also, web resources can be specified to only be loaded from the network. This is done by adding a "NETWORK: " header section before the resources. This functionality can be used to scope down the number of resources that can be accessed from the network, thus, creating an allowed only list (as shown previously).

|Section|Description|
|:------|:----------|
|CACHE|This is the default section for entries. Files listed under this header (or immediately after the CACHE MANIFEST) will be explicitly cached after they're downloaded for the first time.|
|NETWORK|Files listed under this section are white-listed resources that require a connection to the server. All requests to these resources bypass the cache, even if the user is offline. Wildcards may be used.|
|FALLBACK|An optional section specifying fallback pages if a resource is inaccessible. The first URI is the resource, the second is the fallback. Both URIs must be relative and from the same origin as the manifest file. Wildcards may be used.|

**ApplicationCache** functionality is independent of HTTP caching headers. The manifest file implicitly includes itself as a page to be cached. It also needs to have the same domain of origin as the page that contains it.

## Notes

### Limitations

The [specification](http://www.whatwg.org/specs/web-apps/current-work/multipage/offline.html) states that browsers "should consider applying constraints on disk usage". [The disk usage constraints vary across browsers.](http://www.browserscope.org/user/tests/table/agt1YS1wcm9maWxlcnINCxIEVGVzdBjwwK0RDA?v=3&layout=simple)

## Related specifications

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft

## See also

### External resources

-   [Application Cache is a Douchebag](http://alistapart.com/article/application-cache-is-a-douchebag)
-   [HTML5Rocks - A Beginner's Guide to Using the Application Cache](http://www.html5rocks.com/en/tutorials/appcache/beginner/)
-   [Taking your web sites and apps offline with the HTML5 appcache](http://www.webdirections.org/blog/get-offline/)
-   [Running your web applications offline with HTML5 AppCache](http://dev.opera.com/articles/view/offline-applications-html5-appcache/)
-   [appcachefacts.info](http://appcachefacts.info/)
-   [Cache Manifest Validator](http://manifest-validator.com)
