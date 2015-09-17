---
title: 'nextNode'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NodeIterator.nextNode](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator.nextNode) Article]'
  - 'Microsoft Developer Network: [[nextNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975281(v=vs.85).aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/NodeIterator
    href: /dom/NodeIterator
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/NodeIterator
standardization_status: 'W3C Recommendation'
summary: "The NodeIterator.nextNode() method returns the next node in the set represented by the NodeIterator and advances the position of the iterator within the set.  The first call to nextNode() returns the first node in the set.\n"
tags:
  - API_Object_Methods
  - DOM
uri: dom/NodeIterator/nextNode

---
<p>
</p>
<h2>Summary</h2>
<p>The NodeIterator.nextNode() method returns the next node in the set represented by the NodeIterator and advances the position of the iterator within the set.  The first call to nextNode() returns the first node in the set.
</p><p>This method returns null when there are no nodes left in the set.

</p><p>Method of <a href="/dom/NodeIterator">dom/NodeIterator</a><a href="/dom/NodeIterator">dom/NodeIterator</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var object = object.nextNode(/* see parameter list */);
</pre>
<h2>Parameters</h2>
<h3>oNode</h3>
<dl><dt> Data-type</dt>
<dd> any</dd></dl><p><br/>
Object containing
the next node in the list.
</p>
<h2>Return Value</h2>
<p>Returns an object of type  DOM NodeDOM Node
</p><p>Type: <b>HRESULT</b>
</p><p>This method can return one of these values.
</p>
<table class="wikitable"><tr><th>Return code
</th>
<th>Description
</th></tr><tr><td>S_OK
</td>
<td>The operation completed successfully.
</td></tr><tr><td>InvalidStateError _ERR
</td>
<td>NodeIterator raises this exception if detach has been invoked on the object.
</td></tr></table><p> 
</p><p><a href="/dom/Node"><b>Node</b></a>
</p><p>Object containing
the next node in the list.
</p>
<h2>Examples</h2>
<div class="example">
<pre class="html">
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;NextNode example&lt;/title&gt;
  &lt;script type="text/javascript"&gt;
    function LoseMondays(){
	  var ni = document.createNodeIterator(document.body, NodeFilter.SHOW_TEXT, null, false);
      var txt = ni.nextNode();      //go to first node of our NodeIterator
      while (txt)                   //while text
        {
          if (txt.wholeText.match('Monday') || txt.parentNode.getAttribute('id') == 'Monday')
            {
            txt.parentNode.removeChild(txt);        //remove monday's activity
            }
          txt=ni.nextNode();                        //go to next node
        }
    }
    function refresh()                 
      {
        window.location.reload( false );           //reload our page
      }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;&lt;strong&gt;Harry's weekly diary&lt;/strong&gt;&lt;/p&gt;
    &lt;p&gt;Monday Joe bought a turkey.&lt;/p&gt;
    &lt;p&gt;Tuesday Bill bought a pound of ham.&lt;/p&gt;
    &lt;div&gt;Chuck called in sick Monday.&lt;/div&gt;
    &lt;p id="Monday"&gt;CALL supplier today&lt;/p&gt;
    &lt;p&gt;Wednesday's delivery was delayed.&lt;/p&gt;
    &lt;input type="button" name="reset" value="refresh" onclick="refresh()"/&gt;
    &lt;input type="button" name="cutmonday" value="Lose Mondays" onclick="LoseMondays()"/&gt;
&lt;/body&gt;
&lt;/html&gt;

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>This example shows how to create a <a href="/dom/NodeIterator"><b>NodeIterator</b></a> and move forward through the list of nodes.
</p>
<h3>Syntax</h3>
<p>node = nodeIterator.nextNode();
</p>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=182712">Document Object Model (DOM) Level 2 Traversal and Range Specification</a>, Section 1.2</li></ul><h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://dom.spec.whatwg.org/#dom-nodeiterator-nextnode">DOM</a></dt>
  <dd>Living Standard</dd>
</dl>
