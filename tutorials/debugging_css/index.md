---
title: Debugging CSS
notes:
  - 'List utilities to help debug CSS.'
readiness: 'In Progress'
summary: 'This article lists utilities to help analyze situations where a CSS style we think should be applied is not.'
tags:
  - Tutorials
  - CSS
  - Developer
  - Tools
  - HTML
  - Inheritance
uri: 'tutorials/debugging css'

---
**By [Renoir Boulanger](https://renoirboulanger.com/)**

## <span>Summary</span>

This article lists utilities to help analyze situations where a CSS style we think should be applied is not.

## <span>Content Needed</span>

This topic is in progress, we just ran out of time. If you have the time to write it up, please do. We’re all pitching in here at WPD. Thanks!

Methods for debugging CSS are essential, since CSS errors will not output any error message indicating the source of the issue at hand.

## <span>Avoiding problems in the first place</span>

### <span>Cross browser Idiosyncrasies</span>

As mentioned in previous tutorials Web Browsers come with inbuilt CSS. This default CSS may differ between browsers and hence when viewing a site, unless the site CSS cancels out the browser's CSS there is a chance that the page is displayed differently across browsers, which most often than not it is undesirable.

This problem is avoided by normalizing the browser. This is done by using a set of CSS rules to cancel the web browser default CSS before applying custom CSS. There exist a couple of CSS normalizing files on the net freely available.

## <span>CSS to debug CSS</span>

One of the things that could help in identifying a layout issue or perhaps some complex structure like a CSS based menu one would want to see what is really going on in terms of boxes.

``` css
*{
  outline:1px red solid;
}
```

 Using the above will display an outline around each element on the page indicating the structure, which could help in identifying where certain problems are.

## <span>Isolate the issue</span>

If the problem is in a fully blown site with plenty of HTML/CSS, start commenting out the HTML and CSS rules and try to isolate the issue and perhaps even replicate it and try to find the offending rules.

## <span>WebBrowser tools</span>

At the time of writing Google Chrome/Mozilla Firefox and Internet Explorer come with inbuilt developer tools that could help with debugging. These tools allow to inspect elements and view the CSS applied on them. Furthermore one could disable rules, remove properties, add rules and add properties and view the changes in the browser.

## <span>Notes</span>

-   Need to make summary
-   Need to list more relevant and credible resources

## <span>See also</span>

### <span>External resources</span>

-   [24 ways: Debugging CSS with the DOM inspector](http://24ways.org/2005/debugging-css-with-the-dom-inspector/)
-   [Debugging HTML and CSS with the developer tools](http://bigemployee.com/4-simple-techniques-to-quickly-debug-and-fix-your-css-code-in-almost-any-browser/)
-   [CSS Level 2 : The cascade](http://www.w3.org/TR/CSS2/cascade.html#cascade)
