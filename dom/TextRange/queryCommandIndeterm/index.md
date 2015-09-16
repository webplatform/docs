---
title: 'queryCommandIndeterm'
attributions:
  - 'Microsoft Developer Network: [[queryCommandIndeterm Method](http://msdn.microsoft.com/en-us/library/ie/ms536678(v=vs.85).aspx) Article]'
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
summary: 'Returns a Boolean value that indicates whether the specified command is in the indeterminate state.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/queryCommandIndeterm

---
<p>
</p>
<h2>Summary</h2>
<p>
Returns a Boolean value that indicates whether the specified command is in the indeterminate state.</p><p>Method of <a href="/dom/TextRange">dom/TextRange</a><a href="/dom/TextRange">dom/TextRange</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var Result = document.queryCommandIndeterm(/* see parameter list */);
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
<td>The command is in the indeterminate state.
</td></tr><tr><td>false
</td>
<td>The command is not in the indeterminate state.
</td></tr></table><p> 
</p>
<h2>Examples</h2>
<div class="example">
<pre class="js">
function SetToBold () {
            if (document.queryCommandIndeterm ("bold")) {
                alert ("The 'bold' command is in an indeterminate state.");
            }
            else {
                if (document.queryCommandState ("bold")) {
                    alert ("The bold formatting will be removed from the selected text.");
                }
                else {
                    alert ("The selected text will be displayed in bold.");
                }
            }
            document.execCommand ('bold', false, null);
        }

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>This method is a wrapper function for the command constants. You can obtain an <b>IHTMLDocument2</b> interface using IID_IHTMLDocument2 for the IID.
This method is a wrapper function for the command constants. You can obtain an <b>IHTMLControlRange</b> interface using IID_IHTMLControlRange for the IID.
This method is a wrapper function for the command constants. You can obtain an <b>IHTMLTxtRange</b> interface using IID_IHTMLTxtRange for the IID.
</p>
