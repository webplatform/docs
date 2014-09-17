{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The IDBVersionChangeEvent object represents the event object passed to the [[apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded| upgradeneeded]] event, which fires when a database is opened using a higher version number.}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In this example, properties from the IDBVersionChangeEvent object passed to the [[apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded|upgradeneeded]] event are used by the createDatabaseObjects function (not shown):
|Code=try {
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
|LiveURL=
}}
}}
{{Notes_Section
|Usage=When you open a database, you include a version number.  If the supplied version number is greater than the version of the database on the user's device (if any), an [[apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded|upgradeneeded]] event is fired within the context of a version change transaction.  This context lets you create (or modify) object stores, indexes, ranges, and other database objects.

For more information about transaction types, see [[indexeddb/IDBTransaction/mode|IDBTransaction mode]].
|Notes=The [[apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded|upgradeneeded]] event fires before the [[apis/indexeddb/IDBRequest/onsuccess|success]] event, which can lead to issues when attempting to cache handles.
|Import_Notes= 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=* [http://msdn.microsoft.com/en-us/library/jj154905.aspx Creating and opening IndexedDB objects]
|Manual_sections=
}}
{{Topics|API, IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/IndexedDB/IDBVersionChangeEvent
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx IDBVersionChangeEvent object]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}