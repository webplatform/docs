{{Page_Title| Redirect browsers without JavaScript Support}}
{{Flags
|High-level issues=}}
{{Summary_Section|This is an HTML hack to make pages more friendly to those with JavaScript disabled or with no JavaScript support.}}
{{Concept_Page
|Content=This HTML hack allows users with JavaScript disabled or without JavaScript support to still view web content, just without the convenience of JavaScript. Add this tag to the HTML head (best after the <code><meta charset="utf-8" /></code> tag) and it will create an automatic redirect to the no-JS-friendly site.
{{Single Example
|Language=HTML
|Description=Core code.
|Code=&nbsp;
<noscript><meta http-equiv="refresh" content="0; url=www.example.com/no-js-version"></noscript>
}}
This would alleviate the need for JavaScript to be required for many services to even be used, and it would allow for some degree of dynamic content to still be served to those without JS through CSS and server-side logic. The ''url'' parameter of the <code>content</code> attribute can be any legal URL, even the original one with extra parameters. The whole purpose is to serve a page that has no JavaScript requirement for the browser.

This only validates correctly as HTML5 (plug in the source in the [http://validator.w3.org/check W3C validator tool]).
}}
{{Examples_Section
|Not_required=No
|Examples=This demonstrates an example usage of this hack.

{{Single Example
|Language=HTML
|Description=Initial page, assumes JavaScript support.
|Code=<!-- www.example.com/index.html -->
<!DOCTYPE html>
<html>
  <head>
  <meta charset="utf-8" />
  <noscript><meta http-equiv="refresh" content="0; url=www.example.com/no-js-version.html" /></noscript>
  <!-- Browsers without JavaScript will never see this. -->
  <script type="javascript" src="www.example.com/js/jquery.min.js"></script>
  <script type="javascript" src="www.example.com/js/dynamic.js"></script>
<title>Example Page</title>
</head>
<body></body>
</html>
}}{{Single Example
|Language=JavaScript
|Description=Little helper dynamic script
|Code=// www.example.com/js/dynamic.js
$(function () {
  var div = document.createElement('div');
  div.innerHTML        = 'Content that requires JavaScript to run.';
  div.style.textAlign  = 'center';
  div.style.fontWeight = bold;
  $(body).append(div);
})();
}}{{Single Example
|Language=HTML
|Description=Non-JS version
|Code=<!-- www.example.com/no-js-version.html -->
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
<div>Content that requires absolutely no JavaScript.</div>
</body>
</html>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Topics|Accessibility, Compatibility, Design, HTML, JavaScript, Usability}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}