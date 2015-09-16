---
title: 'queryCommandState'
attributions:
  - 'Microsoft Developer Network: [[queryCommandState Method](http://msdn.microsoft.com/en-us/library/ie/ms536679(v=vs.85).aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Returns a Boolean value that indicates the current state of the command.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/queryCommandState

---
<p>
</p>
<h2>Summary</h2>
<p>
Returns a Boolean value that indicates the current state of the command.</p><p>Method of <a href="/dom/TextRange">dom/TextRange</a><a href="/dom/TextRange">dom/TextRange</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = document.queryCommandState(/* see parameter list */);
</pre>
<h2>Parameters</h2>
<h3>cmdID</h3>
<dl><dt> Data-type</dt>
<dd> BSTR</dd></dl><p><br/><b>String</b> that specifies a command identifier.
</p>
<h2>Return Value</h2>
<p>Returns an object of type  BooleanBoolean
</p><p>Boolean
</p><p><b>Boolean</b> that returns one of the following possible values:
</p>
<table class="wikitable"><tr><th>Return value
</th>
<th>Description
</th></tr><tr><td>true
</td>
<td>The given command has been executed on the object.
</td></tr><tr><td>false
</td>
<td>The given command has not been executed on the object.
</td></tr></table><p> 
</p>
<h2>Examples</h2>
<p>This example feature tests for window.getSelection and if not available (legacy IE versions) falls back to document.selection to create a range object. Then queryCommandState is used to determine if the range object can execute the 'bold' command.
</p>
<div class="example">
<pre class="js">
function makeBold(el){
if(window.getSelection){
	var sel=document.getSelection();
	var range = sel.getRangeAt(0),
  	content = range.extractContents(),
    span = document.createElement('b');
	span.appendChild(content);
	var htmlContent = span.innerHTML;
	range.insertNode(span);
}else{
	var sel=document.selection;
	if(sel){
		var rng=sel.createRange();
		if(rng.queryCommandEnabled('bold')){rng.execCommand('bold',false,null);}
	}	
}
}

</pre>
<p><br/></p>
</div>
<h2>Usage</h2>
<pre> Used to add HTML markup to web documents.
</pre>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>This method is a wrapper function for the command constants. You can obtain an <b>IHTMLDocument2</b> interface using IID_IHTMLDocument2 for the IID.
This method is a wrapper function for the command constants. You can obtain an <b>IHTMLControlRange</b> interface using IID_IHTMLControlRange for the IID.
This method is a wrapper function for the command constants. You can obtain an <b>IHTMLTxtRange</b> interface using IID_IHTMLTxtRange for the IID.
</p>
