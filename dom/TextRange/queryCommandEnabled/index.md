---
title: 'queryCommandEnabled'
attributions:
  - 'Microsoft Developer Network: [[queryCommandEnabled Method](http://msdn.microsoft.com/en-us/library/ie/ms536676(v=vs.85).aspx) Article]'
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
summary: 'Returns a Boolean value that indicates whether a specified command can be successfully executed using execCommand, given the current state of the document.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/queryCommandEnabled

---
<p>
</p>
<h2>Summary</h2>
<p>
Returns a Boolean value that indicates whether a specified command can be successfully executed using execCommand, given the current state of the document.</p><p>Method of <a href="/dom/TextRange">dom/TextRange</a><a href="/dom/TextRange">dom/TextRange</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var Result = document.queryCommandEnabled(/* see parameter list */);
</pre>
<h2>Parameters</h2>
<h3>cmdID</h3>
<dl><dt> Data-type</dt>
<dd> BSTR</dd></dl><p><br/><b>String</b> that specifies a command identifier.
</p><p>see <a rel="nofollow" class="external text" href="http://help.dottoro.com/larpvnhw.php">dottoro.com</a> for a full listing of commands.
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
<td>The command is enabled.
</td></tr><tr><td>false
</td>
<td>The command is disabled.
</td></tr></table><p> 
</p>
<h2>Examples</h2>
<p>The following example is a onClick handler to execute the 'cut' command.
</p>
<div class="example">
<pre class="js">
function execCut(){
if(document.queryCommandEnabled('cut')){
	document.execCommand('cut',false,null);}
}

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>Using <b>queryCommandEnabled</b> ("delete") on a <a href="/dom/TextRange"><b>TextRange</b></a> object returns true, while <b>queryCommandEnabled</b> ("delete") on a <a href="/dom/Document">Document</a> object returns false. However, <b>execCommand</b> ("delete") can still be used to delete the selected text.
This method is a wrapper function for the command constants. You can obtain an <b>IHTMLDocument2</b> interface using IID_IHTMLDocument2 for the IID.
This method is a wrapper function for the command constants. You can obtain an <b>IHTMLControlRange</b> interface using IID_IHTMLControlRange for the IID.
This method is a wrapper function for the command constants. You can obtain an <b>IHTMLTxtRange</b> interface using IID_IHTMLTxtRange for the IID.
</p><p><br/></p><p><br/></p>
<h2>See also</h2>
<h3>Other articles</h3>
<p><a rel="nofollow" class="external text" href="http://help.dottoro.com/larpvnhw.php">help.dottoro.com - Command Reference</a>
</p><p><a rel="nofollow" class="external text" href="http://msdn.microsoft.com/en-us/library/ie/hh801227(v=vs.85).aspx">MSDN Commands A-Z</a>
</p>
