---
title: 'hashchange'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, specs, compat'
readiness: 'In Progress'
tags:
  - Events
uri: dom/Element/hashchange

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
</td>
</tr>
</table>
## Examples

Attaching an event handler to a new **onhashchange** event enables the page to detect when the hash has changed and an AJAX navigation has occurred. See Introducing AJAX Navigations for a more robust example.

``` html
<body onhashchange="HashChangeHandler();">
...
</body>
```

## Notes

### Remarks

In Asynchronous JavaScript and XML (AJAX) applications, client requests that do not trigger traditional page navigation should update the **hash** property. This lets the **Back** button function more predictably. The URL fragment (bookmark) can be set by script. The value is appended to the displayed URL, and the navigation is saved in the browser history. Windows Internet Explorer 8. The browser's **Back** and **Forward** buttons do not generate **onhashchange** events for frames or **iframe**s; instead, the frame is refreshed each time. Web pages hosted in frames or **iframe**s should use their **onload** handler or equivalent to read the current URL hash information from the **location.hash** property and set their states accordingly. When first navigating to a page that contains a hash identifier in the URL, an **onhashchange** event is *not* fired. It is expected that the freshly loaded page can inspect the value of the **location.hash** property to extract the current hash value. After this first page loads, setting the **hash** property will fire the **onhashchange** event as expected. This behavior avoids any negative impact on Web page load performance by removing a possible redundant event. To invoke this event, do one of the following:

-   Set the

[**location.hash**](/dom/Location/hash) (bookmark) property.

-   Navigate to the same page with a different bookmark.

The *pEvtObj* parameter is required for the following interfaces:

-   **HTMLWindowEvents3**

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   Window[Window](/dom/Window)
-   body[body](/html/elements/body)
-   `frameSet`
-   `Introducing AJAX Navigations`
