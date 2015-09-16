---
title: onLine
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'applies to navigator.online propert, not window.online'
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/onLine

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var result = element.onLine;
element.onLine = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

In Windows Internet Explorer 8 and later, the **onLine** property returns `true` if both of the following conditions are true:

-   the system is able to communicate with the network
-   the system is not in global offline mode (Users can modify the global offline state by choosing **Work Offline** on the **File** menu.)

onLine false In Microsoft Internet Explorer 4.0 through Windows Internet Explorer 7, the **onLine** property indicates whether the system is in global offline mode. It does not indicate whether the system can communicate with the network. **onLine** returns `true` if the WWAHost.exe can contact the network, otherwise, it returns `false`. A Metro style app using JavaScript uses event listeners ([**addEventListener**](/dom/EventTarget/addEventListener)) to monitor online and offline events that fire when the state of the window object changes. The offline event fires when the **onLine** property changes from `true` to `false`. The online event fires when the **onLine** property changes from `false` to `true`.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 5.6.10
