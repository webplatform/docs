---
title: 'inRange'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/inrange.htm'
notes:
  - 'Needs summary, specs, and compat'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Element
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: dom/Element/inRange

---
<p><br/></p>

<p>Method of <a href="/dom/Element">dom/Element</a><a href="/dom/Element">dom/Element</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var object = object.inRange(/* see parameter list */);
</pre>
<h2>Parameters</h2>
<h3>Range</h3>
<dl><dt> Data-type</dt>
<dd> any</dd></dl><p><br/><a href="/dom/TextRange"><b>TextRange</b></a> object that might be contained.
</p>
<h2>Return Value</h2>
<p>Returns an object of type  DOM NodeDOM Node
</p><p>Boolean
</p><p><b>Boolean</b> that returns one of the following possible values.
</p>
<table class="wikitable"><tr><th>Return value
</th>
<th>Description
</th></tr><tr><td>true
</td>
<td>Range is contained within or is equal to the TextRange object on which the method is called.
</td></tr><tr><td>false
</td>
<td>Range is not contained within the TextRange object on which the method is called.
</td></tr></table><p> 
</p>
<h2>Examples</h2>
<p>The following example shows how to use the <b>inRange</b> method to show that two <a href="/dom/TextRange"><b>TextRange</b></a> objects are equal.
</p>
<div class="example">
<pre class="html">
&lt;html&gt;
&lt;script type="text/javascript"&gt;
window.onload=fnCheck;
function fnCheck(){
    var oRng1 = document.body.createTextRange();
    var oRng2 = oRng1.duplicate();
    var bInside = oRng1.inRange(oRng2); // returns true;
}
&lt;/script&gt;
   
&lt;body&gt;
    &lt;div id=div1&gt;
    Content for division 1.
    &lt;/div&gt;
    &lt;div id=div2&gt;
    Content for division 2.
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;

</pre>
<p><br/></p>
</div>
<p>The following example shows how to use the <b>inRange</b> method to show that two contained ranges are not equal.
</p>
<div class="example">
<pre class="html">
&lt;html&gt;
&lt;script type="text/javascript"&gt;
window.onload=fnCheck;
function fnCheck(){
  	 var oRng1 = document.body.createTextRange(); // create a text range
	   var oRng2 = oRng1.duplicate();		// create a duplicate range base on oRng1

    oRng1.moveToElementText(document.getElementById("div1"));
    oRng2.moveToElementText(document.getElementById("div2"));
    var bInside = oRng1.inRange(oRng2); // returns false;
}
&lt;/script&gt;
   
&lt;body&gt;
    &lt;div id="div1"&gt;
    Content for division 1.
    &lt;/div&gt;
    &lt;div ID="div2"&gt;
    Content for division 2.
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;

</pre>
<p><br/></p>
</div>
<p>The following example shows how to use the <b>inRange</b> method to show that a text range exists within another text range.
</p>
<div class="example">
<pre class="html">
&lt;html&gt;
&lt;script type="text/javascript"&gt;
window.onload=fnCheck;
function fnCheck(){
    var oRng1 = document.body.createTextRange();
    var oRng3 = oRng1.duplicate();
    oRng3.findText('division 1');
    var bInside = oRng1.inRange(oRng3); // returns true; 
}
&lt;/script&gt;
&lt;body&gt;
    &lt;div id="div1"&gt;
    Content for division 1.
    &lt;/div&gt;
    &lt;div ID="div2"&gt;
    Content for division 2.
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/inrange.htm">View live example</a>
</p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>This feature might not be available on platforms other than Microsoft Win32.
</p>
<h3>Syntax</h3>
<h3>Standards information</h3>
<p>There are no standards that apply here.
</p><p><br/></p>
<h2>See also</h2>
<h3>Related pages</h3>
<ul><li>TextRange<a href="/dom/TextRange">TextRange</a></li>
<li>isEqual<a href="/dom/Element/isEqual">isEqual</a></li></ul>
