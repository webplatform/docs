---
title: 'readyState'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec, and compat'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Element/readyState

---
<p><br/></p>
<div class="editors-only">
<p><b>Needs Summary</b>:   This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article. 
</p>
</div>
<div data-template="API_Object_Property">
<p><br/></p><p><br/></p><p>Property of <a href="/dom/Element">dom/Element</a><a href="/dom/Element">dom/Element</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = element.readyState;
element.readyState = value;
</pre>
<p><br/></p>
</div>
<div class="editors-only">
<p><b>Needs Examples</b>:  This section should include examples. 
</p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>The <a href="/apis/file/FileReader"><b>FileReader</b></a> object can be in one of three states.
</p>
<table class="wikitable"><tr><th>Constant
</th>
<th>Value
</th>
<th>Description
</th></tr><tr><td>EMPTY
</td>
<td>0
</td>
<td>The <a href="/apis/file/FileReader"><b>FileReader</b></a> object has been constructed, and there are no pending reads. None of the read methods have been called. This is the default state of a newly created <b>FileReader</b> object, until one of the read methods has been called on it.
</td></tr><tr><td>LOADING
</td>
<td>1
</td>
<td>A <a href="/apis/file/File"><b>File</b></a> or <a href="/apis/file/Blob"><b>Blob</b></a> is being read. One of the read methods is being processed, and no error has occurred during the read.
</td></tr><tr><td>DONE
</td>
<td>2
</td>
<td>The entire <a href="/apis/file/File"><b>File</b></a> or <a href="/apis/file/Blob"><b>Blob</b></a> has been read into memory, a file error occurred during read, or the read was aborted using <a href="/apis/file/FileReader/abort"><b>abort</b></a>. The <a href="/apis/file/FileReader"><b>FileReader</b></a> is no longer reading a <b>File</b> or <b>Blob</b>. If <code>readyState</code> is set to <code>DONE</code> it means at least one of the read methods have been called on this <b>FileReader</b> object.
</td></tr></table><p> 
</p>
<h3>Syntax</h3>
<h2>See also</h2>
<h3>Related pages</h3>
<ul><li>FileReader<a href="/apis/file/FileReader">FileReader</a></li></ul>
