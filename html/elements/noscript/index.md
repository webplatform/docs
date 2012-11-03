== Summary ==

The HTML NoScript Element (<noscript>) defines a section of html to be inserted if a script type on the page is unsupported or if scripting is currently turned off in the browser.

== Specifications ==

* [http://www.w3.org/TR/html5/scripting-1.html#the-noscript-element HTML 5, section 4.3.2]
* [http://www.w3.org/TR/html401/interact/scripts.html#h-18.3.1#HTML 4.01, section 18.3.1]

===Example===

<syntaxhighlight lang="html5" highlight="1-3">
<noscript>
For full functionality of this site it is necessary to enable JavaScript. Here are the <a href="http://www.enable-javascript.com/" target="_blank">instructions how to enable JavaScript in your web browser</a>.
</noscript>
<a href="http://www.webplatform.org/">Webplatform Rocks!</a>
</syntaxhighlight>

When the user has JavaScript turned off in the browser, it will show the text in the <noscript>tag.