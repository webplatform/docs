---
title: 'a'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/a)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5281100'
compatibility:
  feature: a
  topic: html
notes:
  - 'Add more example'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLAnchorElement](/dom/HTMLAnchorElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Defines a hyperlink, a destination of hyperlink, or both.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/a

---
<p>
</p>
<h2>Summary</h2>
<p>
Defines a hyperlink, a destination of hyperlink, or both.</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLAnchorElement">HTMLAnchorElement</a></dd>
</dl><h3>Description</h3>
<p>The <code>a</code> element defines a hyperlink to any content, which could be an external site, another page on the same site, a section within the same page, an image, or a local file.
</p>
<h3>Syntax</h3>
<pre>&lt;a href="[URI]"&gt;[Anchor text or image tag]&lt;/a&gt;</pre>
<pre>&lt;a id="#[identifier]"&gt;[Anchor text or image tag]&lt;/a&gt;</pre>
<pre>&lt;a&gt;[Anchor text or image tag]&lt;/a&gt;</pre>
<h3>Enclosed HTML</h3>
<p>HTML enclosed by the <code>&lt;a&gt;&lt;/a&gt;</code> tags is typically text or an image. It is displayed in the page and (if the <a href="/html/attributes/href">href</a> attribute is present) is rendered as a link.
</p>
<h3>Common Attributes</h3>
<table class="wikitable"><tr><th> Name
</th>
<th> Value
</th>
<th> Purpose
</th>
<th> Example
</th>
<th> Validity
</th></tr><tr><td> <a href="/html/attributes/download"><b>download</b></a>
</td>
<td> text
</td>
<td> File name to show in Save dialog
</td>
<td> <pre>download="filename.pdf"</pre>
</td>
<td> HTML5
</td></tr><tr><td> <a href="/html/attributes/href"><b>href</b></a>
</td>
<td> <a rel="nofollow" class="external text" href="http://www.w3.org/Addressing/URL/uri-spec.html">URI</a>
</td>
<td> Target of link
</td>
<td> <pre>href="http://example.com"</pre> <pre>href="#TableOfContents"</pre>
</td>
<td>  
</td></tr><tr><td> <a href="/html/attributes/id"><b>id</b></a>
</td>
<td> identifier text
</td>
<td> Creates an anchor in the page that can be referred to by href
</td>
<td> <pre>id="TableOfContents"</pre>
</td>
<td>  
</td></tr><tr><td> <a href="/html/attributes/hreflang"><b>hreflang</b></a>
</td>
<td> Language tag <a rel="nofollow" class="external text" href="http://www.ietf.org/rfc/bcp/bcp47.txt">for HTML5</a> or <a rel="nofollow" class="external text" href="http://www.ietf.org/rfc/rfc1766.txt">for HTML4</a>
</td>
<td> Hint for language of target. May be used with rel="alternate" as a hint to the server for which language to provide.
</td>
<td> <pre>hreflang="ja"</pre>
</td></tr><tr><td> <a href="/html/attributes/rel"><b>rel</b></a>
</td>
<td> comma-separated list of keywords
</td>
<td> Indicates the relationship of the link target to the current page
</td>
<td> <pre>rel="help"</pre>
</td>
<td>  
</td></tr><tr><td> <a href="/html/attributes/target"><b>target</b></a>
</td>
<td> <a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/browsers.html#valid-browsing-context-name-or-keyword">Browsing context</a>
</td>
<td> Tells where to open the link when it is followed
</td>
<td> <pre>target="_blank"</pre>
</td>
<td>  
</td></tr></table><h2>Examples</h2>
<div class="example">
<pre class="html">
&lt;!-- Link to an external website. --&gt;
&lt;a href="http://www.example.com"&gt;Example website&lt;/a&gt;

&lt;!-- Link to an internal website in same directory. --&gt;
&lt;a href="home.html"&gt;Home&lt;/a&gt;

&lt;!-- Download link (HTML5 only). Value of download attribute is used as pre-filled file name in Save dialog.
    If no value is specified for the download, the name of the resource will be used.--&gt;
&lt;a href="filename_on_server.pdf" download="meaningful_filename.pdf"&gt;Download your pdf&lt;/a&gt;

&lt;!-- Open a link in the window specified by the attribute TARGET. --&gt;
&lt;a href="http://www.example.com" target="_blank"&gt;Open example website in new window&lt;/a&gt;

&lt;!-- Include an IMG element as a part of the link. --&gt;
&lt;a href="http://www.example.com"&gt;&lt;img src="images/bullet.png"&gt;A link with an image&lt;/a&gt;

&lt;!-- Link to an anchor on the same page. --&gt;
&lt;a href="#top"&gt;Go to top&lt;/a&gt;

&lt;!-- Define an anchor. --&gt;
&lt;a id="top"&gt;&lt;/a&gt;

&lt;!-- Invoke a JavaScript function (Not recommended) --&gt;
&lt;a href="javascript:alert('Link clicked')"&gt;Click this link&lt;/a&gt;

&lt;!-- Links to a document and uses the ''rel'' attribute to specify the relationship to the linked document. --&gt;
&lt;a href="http://www.example.com/help" rel="help"&gt;Link to help&lt;/a&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://gist.github.com/5281100">View live example</a>
</p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>For creating an anchor in the page, the <a href="/html/attributes/name"><b>name</b></a> attribute is obsolete and should be replaced by <a href="/html/attributes/id"><b>id</b></a> attribute.
</p><p>Both text and images can be included within an anchor. An image that is an anchor has a border whose color indicates whether the link has been visited.  To prevent this border from appearing, you can set the <b>img</b> element's <a href="/html/attributes/border"><b>border</b></a> attribute to 0 or omit the <b>border</b> attribute.  You can also use CSS attributes to override the default appearance of <b>a</b> and <b>img</b> elements.
</p><p>The URI may refer to any protocol, e.g. http, mailto, file. A fragment (# followed by text) refers to a location in the current page. href may be omitted to indicate a placeholder link, such as a reference to the current page in a menu.
</p><p>Optionally the <a href="/html/attributes/rel"><b>rel</b></a> element may be specified to provide semantic meaning to the link target.
</p><p>Internationalization topics related to the <code>a</code> element:
</p>
<ul><li> <a rel="nofollow" class="external text" href="http://www.w3.org/International/techniques/authoring-html#linkdestination">Indicating the language of a link destination</a></li></ul><h3>Clicking and focus</h3>
<p>Whether clicking on an anchor causes it to (by default) become focused varies by browser and OS.
</p><p>Does clicking on an anchor give it the focus?
</p>
<table class="wikitable"><tr><th>Desktop Browsers
</th>
<td>Windows 8.1
</td>
<td>OS X 10.9
</td></tr><tr><th>Firefox 30.0
</th>
<td>Yes
</td>
<td>Yes
</td></tr><tr><th>Chrome <a rel="nofollow" class="external text" href="https://code.google.com/p/chromium/issues/detail?id=388666">&gt;=39</a>
</th>
<td>Yes
</td>
<td>Yes
</td></tr><tr><th>Safari 7.0.5
</th>
<td>N/A
</td>
<td>Only when it has a <a href="/html/attributes/tabIndex"><code>tabindex</code></a>
</td></tr><tr><th>Internet Explorer 11
</th>
<td>Yes
</td>
<td>N/A
</td></tr><tr><th>Presto (Opera 12)
</th>
<td>Yes
</td>
<td>???
</td></tr></table><p>Does tapping on an anchor give it the focus?
</p>
<table class="wikitable"><tr><th>Mobile Browsers
</th>
<td>iOS 7.1.2
</td>
<td>Android 4.4.4
</td></tr><tr><th>Safari Mobile
</th>
<td>Only when it has a <a href="/html/attributes/tabIndex"><code>tabindex</code></a>
</td>
<td>N/A
</td></tr><tr><th>Chrome 35
</th>
<td>???
</td>
<td>Only when it has a <a href="/html/attributes/tabIndex"><code>tabindex</code></a>
</td></tr></table><p> 
</p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html51/text-level-semantics.html#the-a-element">HTML 5.1</a></dt>
  <dd>W3C Working Draft</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/text-level-semantics.html#the-a-element">HTML 5</a></dt>
  <dd>W3C Recommendation</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html401/struct/links.html#edef-A">HTML 4.01</a></dt>
  <dd>W3C Recommendation</dd>
</dl>
