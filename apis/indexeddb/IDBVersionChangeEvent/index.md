{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The IDBVersionChangeEvent object represents the event object passed to the [[apis/indexeddb/IDBOpenDBRequest/onupgradeneeded| upgradNeeded]] event, which fires when a database is opened using a higher version number.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=When you open a database, you include a version number.  If the supplied version number is greater than the version of the database on the user's device (if any), an [[apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded|upgradeneeded]] event is fired within the context of a version change transaction.  This context lets you create (or modify) object stores, indexes, ranges, and other database objects.

For more information about transaction types, see [[indexeddb/IDBTransaction/mode|IDBTransaction.mode]].
|Notes=The [[apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded|upgradeneeded]] event fires before the [[apis/indexeddb/IDBRequest/onsuccess|success]] event, which can lead to issues when attempting to cache handles.
|Import_Notes====Members===
The '''IDBVersionChangeEvent''' object has these types of members:
*[#properties Properties]


====Properties====
The '''IDBVersionChangeEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/indexedDB/properties/newVersion|'''newVersion''']]
|Returns the new version number associated with a database.
|-
|[[apis/indexedDB/properties/oldVersion|'''oldVersion''']]
|Returns the old version number associated with a database.
|}
 
 
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/IndexedDB/IDBVersionChangeEvent
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}