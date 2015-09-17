---
title: 'deleteObjectStore'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/indexeddb/IDBDatabase
    href: /apis/indexeddb/IDBDatabase
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/indexeddb/IDBDatabase
summary: 'Destroys an object store with the given name as well as all indexes that are referencing that object store.'
tags:
  - API_Object_Methods
  - API
  - IndexedDB
  - Needs_Examples
uri: apis/indexeddb/IDBDatabase/deleteObjectStore

---
<p><br/></p>
<h2>Summary</h2>
<p>
Destroys an object store with the given name as well as all indexes that are referencing that object store.</p><p>Method of <a href="/apis/indexeddb/IDBDatabase">apis/indexeddb/IDBDatabase</a><a href="/apis/indexeddb/IDBDatabase">apis/indexeddb/IDBDatabase</a>
</p>
<h2>Syntax</h2>
<pre class="js">
var object = object.deleteObjectStore(name);
</pre>
<h2>Parameters</h2>
<h3>name</h3>
<dl><dt> Data-type</dt>
<dd> Blob</dd></dl><p><br/>
Name of the object store to be removed.
</p>
<h2>Return Value</h2>
<p>Returns an object of type  DOM NodeDOM Node
</p><p>This method can throw the following <a href="/dom/DOMException"><b>DOMException</b></a> exceptions:
</p><p><b>Note</b>  As of Internet Explorer 10, the <b>code</b> property is deprecated in lieu of the <b>name</b> property, which is preferred for standards compliance and future compatibility.
</p>
<table class="wikitable"><tr><th>Exception properties
</th>
<th>Description
</th></tr><tr><td>name: InvalidStateError
<p>code: DOMException.INVALID_STATE_ERR (11)
</p>
</td>
<td>The method was not called within the context of a VERSION_CHANGE transaction or the request was made for an object that has been moved or deleted.
</td></tr><tr><td>name: NotFoundError
<p>code: DOMException.NOT_FOUND_ERR (8)
</p>
</td>
<td>An object store could not be found with the specified name (case-sensitive).
</td></tr></table><p> 
</p>

<p><br/></p>
<h3>Syntax</h3>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?LinkId=224519">Indexed Database API</a></li></ul>
