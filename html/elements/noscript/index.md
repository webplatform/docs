---
title: 'noscript'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'https://rawgithub.com/WebPlatformDocs/6364342/raw/47a37f3fe0d920a0c6a8a7974dca473589f1e4f5/dabblet.html'
compatibility:
  feature: noscript
  topic: html
notes:
  - 'See to make the listing of events, methods etc to be generated automatically instead of being hardcoded.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The HTML NoScript Element (&lt;noscript&gt;) defines a section of html to be inserted if a script type on the page is unsupported or if scripting is currently turned off in the browser.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/noscript

---
## Summary

The HTML NoScript Element (&lt;noscript&gt;) defines a section of html to be inserted if a script type on the page is unsupported or if scripting is currently turned off in the browser.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

The *noscript* element content will not be visible if scripting is enabled in the browsers. It is used to present different contents and guide the user on what he should be seeing.

The *noscript* element is not permitted in XML modes.

If you need to display a message to non-scripting user-agents, consider a "loading" message that gets removed by scripting.

## Examples

You must disable javascript for this to work.

``` html
<script>
    /* Do stuff with JavaScript */
</script>
<noscript>
For full functionality of this site it is necessary to enable JavaScript. Here are the <a href="http://www.enable-javascript.com/" >instructions how to enable JavaScript in your web browser</a>.
</noscript>
```

[View live example](https://rawgithub.com/WebPlatformDocs/6364342/raw/47a37f3fe0d920a0c6a8a7974dca473589f1e4f5/dabblet.html)

## Notes

Browsers that don't support the noscript tag will render the content regardless of whether the javascript is supported

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/scripting-1.html#the-noscript-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/scripting-1.html#the-noscript-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/scripts.html#edef-NOSCRIPT)
:   W3C Recommendation
