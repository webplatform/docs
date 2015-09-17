---
title: 'Proxy-based browsers'
notes:
  - 'This is not a web development concept topic, and will attract vendor spam. Deletion candidate.'
readiness: 'Not Ready'
summary: 'This article will give an overview of proxy based browsers. Some solution transform web pages into compact formats. Some solution only provides data compression.'
tags:
  - Concept_Pages
  - Mobile
uri: 'concepts/Internet and Web/proxy based browsers'

---
## Summary

This article will give an overview of proxy based browsers. Some solution transform web pages into compact formats. Some solution only provides data compression.

## Purpose

Proxy Based web browsers reduce bandwidth usage by compressing resources of the rendered page on a proxy server (usually the browser vendors), before sending it to the client browser.

To make a request:

1.  The client requests a page from the Proxy Server.
2.  The proxy server requests the page from the origin server.
3.  The proxy server renders the page / runs javascript /compresses the page (the methods vary between implementations).
4.  The proxy server sends the client the rendered page.
5.  Client interaction with page is sent to the proxy server, who forwards it onto the origin server.

## Concerns

-   Each implementation has different feature support.
-   There may be concerns about trusting a third party service with browsing data.

## Implementations

-   Opera Mini [[1]](http://www.opera.com/mobile/)
-   Opera Desktop with Turbo [[2]](http://www.opera.com/browser/turbo/)
-   Kindle Fire Silk

> All of the browser subsystems are present on your Kindle Fire as well as on the AWS cloud computing platform. Each time you load a web page, Silk makes a dynamic decision about which of these subsystems will run locally and which will execute remotely.

-   Bolt [[3]](http://boltbrowser.com/)
-   Skyfire [[4]](http://www.skyfire.com/)
-   Nokia Xpress Browser [[5]](http://www.nokia.com/ie-en/apps/apps-by-nokia/xpressbrowser/)
-   UC Browser [[6]](http://www.ucweb.com)
