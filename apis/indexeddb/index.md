---
title: 'Indexed Database API'
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'IndexedDB is a client side storage API that persists data in a user''s browser. It is a transactional, non-relational storage mechanism that saves key-value pairs in Object Stores and allows searching data using indexes.'
tags:
  - API_Listings
  - API
  - IndexedDB
uri: apis/indexeddb

---
## Summary

IndexedDB is a client side storage API that persists data in a user's browser. It is a transactional, non-relational storage mechanism that saves key-value pairs in Object Stores and allows searching data using indexes.

[IDBCursor](/apis/indexeddb/IDBCursor)
:   Iterates over object stores and indices.

[IDBFactory](/apis/indexeddb/IDBFactory)
:   The object type for the [indexedDB](/apis/indexeddb/indexedDB) property, which provides access to the IndexedDB features supported by the browser and/or device.

[IDBVersionChangeEvent](/apis/indexeddb/IDBVersionChangeEvent)
:   The IDBVersionChangeEvent object represents the event object passed to the [upgradeneeded](/apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded) event, which fires when a database is opened using a higher version number.

## Usage

     IndexedDB enables you to store large amounts of data in a reliable and structured way. If you are building web applications that need to work offline the API can be useful to store, group, iterate, search, and filter JavaScript objects.

## Notes

The IndexedDB specification supports an Asynchronous API on the window object and a Synchronous API for Webworkers.

An IndexedDB database is made up of Object Stores. Object stores can be created and JavaScript objects of any shape can be stored inside of them. Every object can have different properties, just because they are in the same Object Store it doesn't mean that they need to have the same structure. The only requirement is that the object has properties that match any explicit Keys or Indexes that you have set up on the Object store.

### Constructs

#### Database

Each [origin](http://www.w3.org/TR/html5/browsers.html#origin) has a set of associated databases. Database comprise of Object Stores that store data

#### Object Store

Object Stores have list of records which hold data as key-value pairs. Every Object Store belongs to a database.

#### Keys

Every record in an object store is stored as key-value pairs. Keys are indexed for easy retrieval of data. A valid key can be an [Array](http://www.w3.org/TR/IndexedDB/#bib-ECMA-262), [Date](http://www.w3.org/TR/IndexedDB/#bib-ECMA-262), [DOMString](http://www.w3.org/TR/IndexedDB/#bib-WEBIDL) or [float](http://www.w3.org/TR/IndexedDB/#bib-WEBIDL). Keys can either be generated automatically using a key generator, or specified during data insertion. Keys can also be derived from values using a key path attribute specified for an Object Store

#### Values

Every record has a value that contains the data for a record. A value must be supported by the [Structured Cloning Algorithm](http://www.w3.org/TR/IndexedDB/#bib-HTML5).

#### Index

An index allows looking up records in an object store using properties of the values in the object stores records. An index is a specialized persistent key-value storage and has a referenced object store. The index has a list of records which hold the data stored in the index. The records in an index are automatically populated whenever records in the referenced object store are inserted, updated or deleted. There can be several indexes referencing the same object store, in which changes to the object store cause all such indexes to get updated.

#### Cursor

A cursor is a transient construct to iterate over the records in a database. Cursors can be used on Object Stores or Indexes

#### Transaction

All database read and write operations occur in transactions. Transactions can be read or read\_write. A version\_change transaction is a special transaction that allows adding or deleting Object Stores or Indexes.

#### Request

Each reading and writing operation on a database is done using a request. The result of a request is usually available in success or error events raised on the request.

### Security

The IndexedDB storage follows the same-origin policy.

An IndexedDB database is unique for our domain. So if we set up a database only we are going to be able to see it and the Object stores inside of it. If you use a shared domain, then everyone sharing your domain will be able to access and work with the data in your IndexedDB.

### Storage Limits

-   Firefox will just ask the user for permission for blobs bigger than 50 MB. [Reference](http://support.mozilla.org/en-US/questions/818987)
-   For Google Chrome, see the [reference on temporary storage](https://developers.google.com/chrome/whitepapers/storage#temporary)
-   Internet Explorer will ask the user for permission for Data Stores bigger than 10MB Users can also choose to allow websites to exceed the quota. Users can also change the default 10mb quota in Internet Options \> Browsing History \> Settings \> Caching and Databases. Enterprises can also increase this setting globally or per domain using Group Policy.
-   Windows 8 Apps Each app has a quota of 250MB. Among all apps on the device, the limit is 4% of the disk size or 20GB, whichever is smaller. For hard drives that are less than 30GB, the limit among all apps on the device is 375MB. Because of the overall quota among all apps, test your app to ensure it functions properly when it can store very little or even no data because other apps consume the overall quota. See: [[1]](http://msdn.microsoft.com/en-us/library/windows/apps/jj553412.aspx)

## See also

### Other articles

Tutorials and Walkthroughs:

-   [MDN: Storing images and files in IndexedDB](http://hacks.mozilla.org/2012/02/storing-images-and-files-in-indexeddb/)
-   [HTML5 Rocks: A simple TODO list using HTML5 IndexedDB](http://www.html5rocks.com/en/tutorials/indexeddb/todo/)
-   [MSDN: How to create a tag cloud using IndexedDB](http://msdn.microsoft.com/en-us/library/ie/jj154908(v=vs.85).aspx)

### External resources

-   [W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)

### Library

-   [IDBWrapper](https://github.com/jensarps/IDBWrapper) Ease the use of indexedDB and abstract away the differences between the existing implementations in Chrome, Firefox and IE10 (yes, it works in all three). Show how IDB works. The code is split up into short methods, so that it's easy to see what happens in what method.[[2]](https://github.com/jensarps/IDBWrapper)

-   [YDN-DB](https://github.com/yathit/ydn-db) Javascript database module for Indexeddb, Web SQL and localStorage storage mechanisms supporting version migration, advanced query, SQL and transaction. [API Documentations](http://dev.yathit.com/api-reference/ydn-db/storage.html)
