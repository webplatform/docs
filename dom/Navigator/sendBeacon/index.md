---
title: 'sendBeacon'
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://updates.html5rocks.com/2014/10/Send-beacon-data-in-Chrome-39)'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Navigator
    href: /dom/Navigator
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/Navigator
standardization_status: 'W3C Working Draft'
summary: 'Asynchronously queues small amounts of HTTP data for transfer from the user agent to a web server. For example, it can be used to send analytics or diagnostics code without delaying the page''s unload or affecting the performance of the navigation.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - WebRTC
uri: dom/Navigator/sendBeacon

---
<p>
</p>
<h2>Summary</h2>
<p>
Asynchronously queues small amounts of HTTP data for transfer from the user agent to a web server. For example, it can be used to send analytics or diagnostics code without delaying the page's unload or affecting the performance of the navigation.</p><p>Method of <a href="/dom/Navigator">dom/Navigator</a><a href="/dom/Navigator">dom/Navigator</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = navigator.sendBeacon(url, data);
</pre>
<h2>Parameters</h2>
<h3>url</h3>
<dl><dt> Data-type</dt>
<dd> any</dd></dl><p><br/>
DOMString
</p><p><br/></p>
<h3>data</h3>
<dl><dt> Data-type</dt>
<dd> any</dd></dl><p><br/>
Must be of one of the following types:
</p>
<ul><li>ArrayBufferView</li>
<li>Blob</li>
<li>DOMString</li>
<li>FormData</li></ul><h2>Return Value</h2>
<p>Returns an object of type  BooleanBoolean
</p><p>Boolean
</p><p><b>Boolean</b>. Returns one of the following possible values:
</p>
<table class="wikitable"><tr><th>Return value
</th>
<th>Description
</th></tr><tr><td>true
</td>
<td>The HTTP data was queued for transfer.
</td></tr><tr><td>false
</td>
<td>The HTTP data was not queued for transfer.
</td></tr></table><p> 
</p>
<h2>Examples</h2>
<p>This example queues data for the server on the pagehide event.
</p>
<div class="example">
<pre class="js">
function() {
  window.addEventListener('pagehide', logData, false);
  function logData() {
    navigator.sendBeacon(
      'https://putsreq.herokuapp.com/Dt7t2QzUkG18aDTMMcop',
       'Sent by a beacon!');
   }
}();

</pre>
<p><br/></p>
</div>
<p><br/></p><p><br/></p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/beacon/">Beacon</a></dt>
  <dd>W3C Working Draft</dd>
</dl>
