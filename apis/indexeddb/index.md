{{Page_Title|IndexedDB reference}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Needed, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|IndexedDB is a client side storage API that persists data in a user's browser. It is a transactional, non-relational storage mechanism that saves key-value pairs in Object Stores and allows searching data using indexes.}}
{{API_Listing
|Use_page_title=Yes
|List_all_subpages=Yes
}}
{{Notes_Section
|Usage=indexedDB = window.indexedDB;
|Notes=The IndexedDB specification supports an Asynchronous API on the window object and a Synchronous API for Webworkers.

=== Constructs ===

==== Database ====
Each [http://www.w3.org/TR/html5/browsers.html#origin origin] has a set of associated databases. Database comprise of Object Stores that store data

==== Object Store ====
Object Stores have list of records which hold data as key-value pairs. Every Object Store belongs to a database.

==== Keys ====
Every record in an object store is stored as key-value pairs. Keys are indexed for easy retrieval of data. 
A valid key can be an [http://www.w3.org/TR/IndexedDB/#bib-ECMA-262 Array], [http://www.w3.org/TR/IndexedDB/#bib-ECMA-262 Date], [http://www.w3.org/TR/IndexedDB/#bib-WEBIDL DOMString] or [http://www.w3.org/TR/IndexedDB/#bib-WEBIDL float]. Keys can either be generated automatically using a key generator, or specified during data insertion. Keys can also be derived from values using a key path attribute specified for an Object Store

==== Values ====
Every record has a value that contains the data for a record. A value must be supported by the [http://www.w3.org/TR/IndexedDB/#bib-HTML5 Structured Cloning Algorithm]. 

==== Index ====
An index allows looking up records in an object store using properties of the values in the object stores records.An index is a specialized persistent key-value storage and has a referenced object store. The index has a list of records which hold the data stored in the index. The records in an index are automatically populated whenever records in the referenced object store are inserted, updated or deleted. There can be several indexes referencing the same object store, in which changes to the object store cause all such indexes to get updated.

==== Cursor ====
A cursor is a transient construct to iterate over the records in a database. Cursors can be used on Object Stores or Indexes

==== Transaction ====
All database read and write operations occur in transactions. Transactions can be read or read_write. A version_change transaction is a special transaction that allows adding or deleting Object Stores or Indexes. 

==== Request ====
Each reading and writing operation on a database is done using a request. The result of a request is usually available in success or error events raised on the request.  

=== Security ===
The IndexedDB storage follows the same-origin policy.

=== Storage Limits ===

*Firefox will just ask the user for permission for blobs bigger than 50 MB. [http://support.mozilla.org/en-US/questions/818987 Reference]
*For Google Chrome, see the [https://developers.google.com/chrome/whitepapers/storage#temporary reference on temporary storage]
}}
{{See_Also_Section
|External_links=* [http://www.w3.org/TR/IndexedDB/ W3C IndexedDB Specification]
|Manual_sections=Wrappers

* IDBStore [https://github.com/jensarps/IDBWrapper]
:#ease the use of indexedDB and abstract away the differences between the existing impls in Chrome, Firefox and IE10 (yes, it works in all three), and [https://github.com/jensarps/IDBWrapper]

:#show how IDB works. The code is split up into short methods, so that it's easy to see what happens in what method.[https://github.com/jensarps/IDBWrapper]
}}
{{Topics|IndexedDB}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
[[Category:API_Listings]]