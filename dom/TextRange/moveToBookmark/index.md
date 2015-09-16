---
title: 'moveToBookmark'
attributions:
  - 'Microsoft Developer Network: [[moveToBookmark Method](http://msdn.microsoft.com/en-us/library/ie/ms536628(v=vs.85).aspx) Article]'
notes:
  - 'needs example'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Almost Ready'
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
summary: 'Moves to a bookmark.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextRange/moveToBookmark

---
<p>
</p>
<h2>Summary</h2>
<p>
Moves to a bookmark.</p><p>Method of <a href="/dom/TextRange">dom/TextRange</a><a href="/dom/TextRange">dom/TextRange</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var result = textRange.moveToBookmark(/* see parameter list */);
</pre>
<h2>Parameters</h2>
<h3>Bookmark</h3>
<dl><dt> Data-type</dt>
<dd> BSTR</dd></dl><p><br/><b>String</b> that specifies the bookmark to move to.
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
<td>Successfully moved to the bookmark.
</td></tr><tr><td>false
</td>
<td>Move to the bookmark failed.
</td></tr></table><p> 
</p>
<div class="editors-only">
<p><b>Needs Examples</b>:  This section should include examples. 
</p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>Bookmarks are opaque strings created with the <a href="/dom/TextRange/getBookmark"><b>getBookmark</b></a> method.
This feature might not be available on non-Microsoft Win32 platforms.
</p>
