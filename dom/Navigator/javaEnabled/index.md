---
title: 'javaEnabled'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[javaEnabled Method](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorPlugins.javaEnabled) Article]'
  - 'Microsoft Developer Network: [[javaEnabled Method](http://msdn.microsoft.com/en-us/library/ie/ms536610(v=vs.85).aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Navigator
    href: /dom/Navigator
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/Navigator
standardization_status: Non-Standard
summary: 'This method indicates whether the current browser is Java Run Time Environment-enabled or not.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Navigator/javaEnabled

---
<p>
</p>
<h2>Summary</h2>
<p>
This method indicates whether the current browser is Java Run Time Environment-enabled or not.</p><p>Method of <a href="/dom/Navigator">dom/Navigator</a><a href="/dom/Navigator">dom/Navigator</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = navigator.javaEnabled();
</pre>
<p><br/></p>
<h2>Return Value</h2>
<p>Returns an object of type  BooleanBoolean
</p><p>Boolean
</p><p><b>Boolean</b>. Returns one of the following possible values:
</p>
<table class="wikitable"><tr><th>Return value
</th>
<th>Description
</th></tr><tr><td>true
</td>
<td>Java JRE is enabled.
</td></tr><tr><td>false
</td>
<td>Java JRE is not enabled.
</td></tr></table><p> 
</p>
<h2>Examples</h2>
<p>Feature test for Java JRE. Negative results do not mean that Java JRE is not installed on the client. It can also indicate that the Java JRE has been disabled by the client Addons Manager or the Java JRE control panel.
</p>
<div class="example">
<pre class="js">
if (window.navigator.javaEnabled()) {
   // browser has java JRE and it is enabled.
}

</pre>
<p><br/></p>
</div>
<h2>Usage</h2>
<pre> Feature testing for Java JRE support.
</pre>
<p>This usage scenario can be unreliable as the client may have disabled JRE.
</p><p>Alternatively use text fallbacks for your applet and object tags that are using Java JRE.
eg.
</p><p>&lt;applet&gt;
your browser does not have Java JRE installed or it has been disabled.
&lt;/applet&gt;
</p><p>&lt;object&gt;
your browser does not have Java JRE installed or it has been disabled.
&lt;/object&gt;
</p><p>Note that the &lt;applet&gt; tag has been depreciated in html5. Use the &lt;object&gt; tag instead.
</p>
<h2>Notes</h2>
<p>This method does NOT determine if javascript or active scripting is enabled in the web browser or not.
To detect if active scripting is enabled in a web browser add &lt;noscript&gt; tags to your web page.
</p><p>The return value for this method indicates whether the preference that controls Java Run Time Environment is on or off - not whether the browser offers Java support in general.
</p><p>Java JRE can also be disabled from the web browser's Addons manager or the Java JRE control panel.
</p><p><br/></p><p><br/></p>
<h2>See also</h2>
<h3>Other articles</h3>
<p><a rel="nofollow" class="external text" href="http://java.com">Download Java JRE from java.com</a>
</p><p><a rel="nofollow" class="external text" href="http://javatester.org">JavaTester.org - All about Java JRE </a>
</p><p><a rel="nofollow" class="external text" href="http://javatester.org/version.html">Test the version of Java JRE your browser is using</a>
</p>
