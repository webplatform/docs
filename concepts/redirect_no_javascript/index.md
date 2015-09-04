---
title: redirect no javascript
tags:
  - Concept
  - Pages
  - Accessibility
  - Compatibility
  - Design
  - HTML
  - JavaScript
  - Usability
readiness: 'In Progress'
summary: 'This is an HTML hack to make pages more friendly to those with JavaScript disabled or with no JavaScript support.'
uri: 'concepts/redirect no javascript'

---
# Redirect browsers without JavaScript Support

## Summary

This is an HTML hack to make pages more friendly to those with JavaScript disabled or with no JavaScript support.

 This HTML hack allows users with JavaScript disabled or without JavaScript support to still view web content, just without the convenience of JavaScript. Add this tag to the HTML head (best after the `<meta charset="utf-8" />` tag) and it will create an automatic redirect to the no-JS-friendly site.

Core code.

``` {.html}
Â
<noscript><meta http-equiv="refresh" content="0; url=www.example.com/no-js-version" /></noscript>
```

This would alleviate the need for JavaScript to be required for many services to even be used, and it would allow for some degree of dynamic content to still be served to those without JS through CSS and server-side logic. The *url* parameter of the `content` attribute can be any legal URL, even the original one with extra parameters. The whole purpose is to serve a page that has no JavaScript requirement for the browser.

This only validates correctly as HTML5 (plug in the source in the [W3C validator tool](http://validator.w3.org/check)).

## Examples

Initial page, assumes JavaScript support.

``` {.html}
<!-- www.example.com/index.html -->
<!DOCTYPE html>
<html>
  <head>
  <meta charset="utf-8" />
  <noscript><meta http-equiv="refresh" content="0; url=www.example.com/no-js-version.html" /></noscript>
  <!-- Browsers without JavaScript will never see this. -->
  <script type="text/javascript" src="www.example.com/js/jquery.min.js"></script>
  <script type="text/javascript" src="www.example.com/js/dynamic.js"></script>
<title>Example Page</title>
</head>
<body></body>
</html>
```

Little helper dynamic script

``` {.js}
// www.example.com/js/dynamic.js
$(function () {
  var div = document.createElement('div');
  div.innerHTML        = 'Content that requires JavaScript to run.';
  div.style.textAlign  = 'center';
  div.style.fontWeight = bold;
  $(body).append(div);
})();
```

Non-JS version

``` {.html}
<!-- www.example.com/no-js-version.html -->
<!-- Browsers with JavaScript support will likely never see this page. -->
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <style type="text/css">
  .center-text {
    text-align: center;
    font-weight: bold;
  }
  <title>Example Page</title>
</head>
<body>
Content that requires absolutely no JavaScript.
</body>
</html>
```

This minimal example demonstrates an example usage of this hack.