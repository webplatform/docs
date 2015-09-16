---
title: 'Redirect browsers without JavaScript Support'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
summary: 'This is an HTML hack to make pages more friendly to those with JavaScript disabled or with no JavaScript support.'
tags:
  - Concept
  - Pages
  - Accessibility
  - Compatibility
  - Design
  - HTML
  - JavaScript
  - Usability
uri: 'concepts/redirect no javascript'

---
<h2>Summary</h2>
<p>
This is an HTML hack to make pages more friendly to those with JavaScript disabled or with no JavaScript support.</p><p><br/>
This HTML hack allows users with JavaScript disabled or without JavaScript support to still view web content, just without the convenience of JavaScript. Add this tag to the HTML head (best after the <code>&lt;meta charset="utf-8" /&gt;</code> tag) and it will create an automatic redirect to the no-JS-friendly site.
</p><p>Core code.
</p>
<div class="example">
<pre class="html">
 
&lt;noscript&gt;&lt;meta http-equiv="refresh" content="0; url=www.example.com/no-js-version" /&gt;&lt;/noscript&gt;

</pre>
<p><br/></p>
</div>
<p>This would alleviate the need for JavaScript to be required for many services to even be used, and it would allow for some degree of dynamic content to still be served to those without JS through CSS and server-side logic. The <i>url</i> parameter of the <code>content</code> attribute can be any legal URL, even the original one with extra parameters. The whole purpose is to serve a page that has no JavaScript requirement for the browser.
</p><p>This only validates correctly as HTML5 (plug in the source in the <a rel="nofollow" class="external text" href="http://validator.w3.org/check">W3C validator tool</a>).
</p>
<h2>Examples</h2>
<p>Initial page, assumes JavaScript support.
</p>
<div class="example">
<pre class="html">
&lt;!-- www.example.com/index.html --&gt;
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
  &lt;meta charset="utf-8" /&gt;
  &lt;noscript&gt;&lt;meta http-equiv="refresh" content="0; url=www.example.com/no-js-version.html" /&gt;&lt;/noscript&gt;
  &lt;!-- Browsers without JavaScript will never see this. --&gt;
  &lt;script type="text/javascript" src="www.example.com/js/jquery.min.js"&gt;&lt;/script&gt;
  &lt;script type="text/javascript" src="www.example.com/js/dynamic.js"&gt;&lt;/script&gt;
&lt;title&gt;Example Page&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;&lt;/body&gt;
&lt;/html&gt;

</pre>
<p><br/></p>
</div>
<p>Little helper dynamic script
</p>
<div class="example">
<pre class="js">
// www.example.com/js/dynamic.js
$(function () {
  var div = document.createElement('div');
  div.innerHTML        = 'Content that requires JavaScript to run.';
  div.style.textAlign  = 'center';
  div.style.fontWeight = bold;
  $(body).append(div);
})();

</pre>
<p><br/></p>
</div>
<p>Non-JS version
</p>
<div class="example">
<pre class="html">
&lt;!-- www.example.com/no-js-version.html --&gt;
&lt;!-- Browsers with JavaScript support will likely never see this page. --&gt;
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;meta charset="utf-8" /&gt;
  &lt;style type="text/css"&gt;
  .center-text {
    text-align: center;
    font-weight: bold;
  }
  &lt;title&gt;Example Page&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div&gt;Content that requires absolutely no JavaScript.&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;

</pre>
<p><br/></p>
</div>

<p>This minimal example demonstrates an example usage of this hack.
</p>
