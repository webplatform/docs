---
title: 'IDBVersionChangeEvent'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBVersionChangeEvent)'
  - 'Microsoft Developer Network: [[IDBVersionChangeEvent object](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'The IDBVersionChangeEvent object represents the event object passed to the  upgradeneeded event, which fires when a database is opened using a higher version number.'
tags:
  0: API
  1: Objects
  3: IndexedDB
uri: apis/indexeddb/IDBVersionChangeEvent

---
<p>
</p>
<h2>Summary</h2>
<p>
The IDBVersionChangeEvent object represents the event object passed to the  upgradeneeded event, which fires when a database is opened using a higher version number.</p><p><br/></p>
<h2>Properties</h2>

<dl><dt>API Name</dt>
  <dd>Summary</dd>
</dl><dl><dt><a href="/apis/indexeddb/IDBVersionChangeEvent/newVersion">newVersion</a></dt>
  <dd>Returns the new version of the database, which is the version specified by the open request.</dd>
</dl><dl><dt><a href="/apis/indexeddb/IDBVersionChangeEvent/oldVersion">oldVersion</a></dt>
  <dd>Returns the old version of the database.</dd>
</dl><p><br/></p>
<h2>Methods</h2>
<p><i>No methods.</i>
</p>
<h2>Events</h2>
<p><i>No events.</i>
</p>
<h2>Examples</h2>
<p>In this example, properties from the IDBVersionChangeEvent object passed to the <a href="/apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded">upgradeneeded</a> event are used by the createDatabaseObjects function (not shown):
</p>
<div class="example">
<pre class="js">
try {
  var req = window.indexedDB.open( "MyDatabase", 1.0 );
  req.onsuccess = doDatabaseWork; 
  req.onerror = handleErrorEvent;
  req.onblocked = handleBlockedEvent;
  req.onupgradeneeded = function(evt) {
    createDatabaseObjects( 
       evt.target.result, evt.target.transaction, 
       evt.oldVersion, evt.newVersion );
  }
} catch( ex ) {
  handleException( ex.message );
}

</pre>
<p><br/></p>
</div>
<h2>Usage</h2>
<pre> When you open a database, you include a version number.  If the supplied version number is greater than the version of the database on the user's device (if any), an <a href="/apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded">upgradeneeded</a> event is fired within the context of a version change transaction.  This context lets you create (or modify) object stores, indexes, ranges, and other database objects.
</pre>
<p>For more information about transaction types, see <a href="/apis/indexeddb/IDBTransaction/mode">IDBTransaction mode</a>.
</p>
<h2>Notes</h2>
<p>The <a href="/apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded">upgradeneeded</a> event fires before the <a href="/apis/indexeddb/IDBRequest/onsuccess">success</a> event, which can lead to issues when attempting to cache handles.
</p><p> 
</p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/IndexedDB/">W3C IndexedDB Specification</a></dt>
  <dd>W3C Proposed Recommendation</dd>
</dl><h2>See also</h2>
<h3>External resources</h3>
<ul><li> <a rel="nofollow" class="external text" href="http://msdn.microsoft.com/en-us/library/jj154905.aspx">Creating and opening IndexedDB objects</a></li></ul>
