---
title: 'Overview of client-side storage'
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/offline/storage/)'
readiness: 'Ready to Use'
summary: 'A high-level overview of modern client-side storage techniques.'
tags:
  - Tutorials
  - IndexedDB
  - Webstorage
uri: 'tutorials/offline storage'

---
**By Michael Mahemoff**
Originally published Oct. 1, 2010

## Summary

A high-level overview of modern client-side storage techniques.

## Introduction

This is an overview of client-side storage, a general term for several separate but related APIs: Web Storage, Web SQL Database, Indexed Database, and File Access. Each of these techniques provides a distinct way to store data on the user's hard drive, instead of the server, where data usually resides. There are two main reasons to do this: (a) to make the web app available offline; (b) to improve performance. For a detailed explanation of the use cases for client-side storage, see the article, ["Offline": What does it mean and why should I care?](http://docs.webplatform.org/wiki/tutorials/about_offline).

The APIs share a similar scope and similar principles. So let's first understand what they have in common before launching to the specifics of each.

## Common Features

### Storage on the Client Device

In practice, "client-side storage" means data is passed to the browser's storage API, which saves it on the local device in the same area as it stores other user-specific information, e.g. preferences and cache. Beyond saving data, the APIs let you retrieve data, and in some cases, perform searches and batch manipulations.

### Sandboxed

All four storage APIs tie data to a single "origin". e.g. if <http://abc.example.com> saves some data, then the browser will only permit <http://abc.example.com> to access that data in the future. When it comes to "origins", the domain must be exactly the same, so <http://example.com> and <http://def.example.com> are both disqualified. The port must match too, so <http://abc.example.com:123> also cannot see <http://abc.example.com> (which defaults to port 80), and so must the protocol (http versus https, etc.).

### Quotas

You can imagine the chaos if any website was allowed to populate unsuspecting hard drives with gigabytes of data! Thus, browsers impose limits on storage capacity. When your app attempts to exceed that limit, the browser will typically show a dialog to let the user confirm the increase. You might expect the browser to enforce a single limit for all storage an origin can use, but the major browsers are actually enforcing limits separately for each storage mechanism. This may change in the future, but for now, you should think of the browser as maintaining a 2-D matrix, with "origin" in one dimension and "storage" in the other. For example, "<http://abc.example.com>" is allowed to store up to 5MB of Web Storage, 25MB of Web SQL Database Storage, and forbidden to use Indexed Database. Another welcome enhancement in this area would be user interfaces to let users view and control how much space they have allocated for each origin.

There are also environments where the user can see upfront how much storage will be used, e.g. in the case of the Chrome Web Store, when a user installs an app, they will be prompted upfront to accept its permissions, which include storage limits. One possible value is "unlimited\_storage".

### Transactions

The two "database" storage formats support transactions. The aim is the same reason regular relational databases use transactions: To ensure the integrity of the database. Transactions prevent "race conditions", a phenomenon where two sequences of operations are applied to the database at the same time, leading to results that are both unpredictable and a database whose state is of dubious accuracy.

### Synchronous and Asynchronous Modes

Most of the storage formats all support synchronous and asynchronous modes. Synchronous mode is blocking, meaning that the storage operation will be executed to completion before the next line of Javascript is executed. Asynchronous mode will cause the next line of Javascript to be executed immediately, with a new thread implicitly created to perform the storage operation. The application will be notified when the operation is finished by way of a callback function being called, a function which must be specified when the call is made.

Synchronous mode is okay for low-impact situations, e.g. maintaining a set of preferences; it's a much simpler programming model, and such operations only take a few milliseconds. But in many production situations, data crunching will block the main thread, which includes the user interface. The display won't update during that time, and the user won't know if their mouse and keyboard actions have been received. So with larger data and complex operations, you should really choose asynchronous mode to keep your app running smoothly. Or alternatively, you can run synchronous operations in a spearate thread using Web Workers. Indeed, aside from Web Storage, you're forced to do it this way; all the other APIs only make their synchronous versions available from inside a Web Worker.

## Overview and Comparison of APIs

### Web Storage

[Web Storage](http://dev.w3.org/html5/webstorage/) is basically a single persistent object called `localStorage`. You can set values using `localStorage.foo = "bar"` and retrieve them later on — even when the browser has been closed and re-opened — as `localStorage.foo`. There's also a second object called `sessionStorage` available, which works the same way, but clears when the window is closed.

Web Storage is an example of a [NoSQL key-value store](http://en.wikipedia.org/wiki/NoSQL#Key-value_store).

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Strengths of Web Storage</th>
<th align="left">Weakness of Web Storage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ol>
<li>Supported on all modern browsers, as well as on iOS and Android, for several years (IE since version 8).</li>
<li>Simple API signature.</li>
<li>Simple call flow, being a synchronous API.</li>
<li>Semantic events available to keep other tabs/windows in sync.</li>
</ol></td>
<td align="left"><ol>
<li>Poor performance for large/complex data, when using the synchronous API (which is the most widely supported mode).</li>
<li>Poor performance when searching large/complex data, due to lack of indexing. (Search operations have to manually iterate through all items.)</li>
<li>Poor performance when storing and retrieving large/complex data structures, because it's necessary to manually serialize and de-serialize to/from string values. The major browser implementations only support string values (even though the spec says otherwise).</li>
<li>Need to ensure data consistency and integrity, since data is effectively unstructured.</li>
</ol></td>
</tr>
</tbody>
</table>

### Web SQL Database

[Web SQL Database](http://www.w3.org/TR/webdatabase/) is a structured database with all the functionality - and complexity - of a typical [SQL-powered relational database](http://en.wikipedia.org/wiki/Structured_Query_Language). Indexed Database sits somewhere between the two. It has free-form key-value pairs, like Web Storage, but also the capability to index fields from those values, so searching is much faster.

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Strengths of Web SQL Database</th>
<th align="left">Weakness of Web SQL Database</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ol>
<li>Supported on major mobile browsers (Android Browser, Mobile Safari, Opera Mobile) as well as several desktop browsers (Chrome, Firefox, Opera).</li>
<li>Good performance generally, being an asynchronous API. Database interaction won't lock up the user interface. (Synchronous API is also available for WebWorkers.)</li>
<li>Good search performance, since data can be indexed according to search keys.</li>
<li>Robust, since it supports a <a href="http://en.wikipedia.org/wiki/Database_transaction">transactional database model</a>.</li>
<li>Easier to maintain integrity of data, due to rigid data structure.</li>
</ol></td>
<td align="left"><ol>
<li>Deprecated. Will not be supported on IE or Firefox, and will probably be phased out from the other browsers at some stage.</li>
<li>Steep learning curve, requiring knowledge of relational databases and SQL.</li>
<li>Suffers from <a href="http://en.wikipedia.org/wiki/Object-relational_impedance_mismatch">object-relational impedence mismatch</a>.</li>
<li>Diminishes agility, as database schema must be defined upfront, with all records in a table matching the same structure.</li>
</ol></td>
</tr>
</tbody>
</table>

### Indexed Database (IndexedDB)

So far, we have seen that Web Storage and Web SQL Database both have major strengths as well as major weaknesses. [Indexed Database](http://www.w3.org/TR/IndexedDB/) has arisen from experiences with both of those earlier APIs, and can be seen as an attempt to combine their strengths without incurring their weaknesses.

An Indexed Database is a collection of "object stores" which you can just drop objects into. The stores are something like SQL tables, but in this case, there's no constraints on the object structure and so no need to define anything upfront. So this is similar to Web Storage, with the advantage that you can have as many databases as you like, and as many stores within each database. But unlike Web Storage, there are important performance benefits: An asynchronous API, and you can create indexes on stores to improve search speed.

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Strengths of IndexedDB</th>
<th align="left">Weakness of IndexedDB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ol>
<li>Good performance generally, being an asynchronous API. Database interaction won't lock up the user interface. (Synchronous API is also available for WebWorkers.)</li>
<li>Good search performance, since data can be indexed according to search keys.</li>
<li>Supports agile development, with no need to flexible data structures.</li>
<li>Robust, since it supports a <a href="http://en.wikipedia.org/wiki/Database_transaction">transactional database model</a>.</li>
<li>Fairly easy learning curve, due to a simple data model.</li>
<li>Decent browser support: Chrome, Firefox, mobile FF, IE10.</li>
</ol></td>
<td align="left"><ol>
<li>Somewhat complex API.</li>
<li>Need to ensure data consistency and integrity, since data is effectively unstructured. (This is the standard flipside weakness to the typical strengths of NOSQL structures.)</li>
</ol></td>
</tr>
</tbody>
</table>

### FileSystem

The previous formats are all suitable for text and structured data, but when it comes to large files and binary content, we need something else. Fortunately, we now have a [FileSystem API standard](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/). It gives each domain a full hierarchical filesystem, and in Chrome at least, these are real files sitting on the user's hard drive. For reading and writing of individual files, the API builds on the existing [File API](http://www.w3.org/TR/FileAPI/).

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Strengths of FileSystem API</th>
<th align="left">Weakness of FileSystem API</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ol>
<li>Can store large content and binary files, so it's suitable for images, audio, video, PDFs, etc.</li>
<li>Good performance, being an asynchronous API.</li>
</ol></td>
<td align="left"><ol>
<li>Very early standard. Only available in Chrome.</li>
<li>No transaction support.</li>
<li>No built-in search/indexing support.</li>
</ol></td>
</tr>
</tbody>
</table>

## Show Me the Code

This section compares how the various APIs tackle the same problem. The example is a "geo-mood" checkin system, where you can track your mood across time and place. The interface lets you switch between database types. Of course, this is slightly contrived as in real world situations, one database type will always make more sense than the rest, and FileSystem API is not suited to this kind of application at all! But for demonstration purposes, it's helpful indeed if we can see the different means we can use to achieve the same end. Note too that some of the code snippets have been refactored for readability.

[Try the Geo-Mood demo now.](http://www.html5rocks.com/en/tutorials/offline/storage/demo.html)

To make the demo interesting, we'll isolate the data storage aspects using [standard object-oriented design techniques](http://en.wikipedia.org/wiki/Polymorphism_in_object-oriented_programming), more specifically [TODO the Strategy pattern]. The UI logic will only know there is a "store"; it won't need to know how the store is implemented, because each store has exactly the same methods on it. So the UI code can just call `store.setup()`, `store.count()`, and so on. In reality, there are four implementations of the store, one for each storage type. When the app starts up, it inspects the URL and instantiates the right store.

To keep the API consistent, the methods are asynchronous, i.e. they pass results back to the caller. This is even true for the Web Storage implementation, where the underlying implementation is local.

In the walkthroughs below, we'll skip the UI and geolocation logic to focus on the storage techniques.

### Setting up the Store

For **localStorage**, we do a simple check to see if the store exists. If not, we'll create a new array and store it against the localStorage "checkins" key. We use JSON to convert the structure to a string first, since, in most browsers, localStorage only stores strings.

    if (!localStorage.checkins) localStorage.checkins = JSON.stringify([]);

For **Web SQL Database**, we need to create the database structure if it doesn't exist. `openDatabase` fortunately creates the database automatically if it doesn't exist, and, likewise, we use the SQL phrase "if not exists" to ensure the new checkins table is not overridden if it is already present. We have to define the structure of the data upfront, i.e. the name and type of each column in the checkins table. Each row will represent a single checkin.

    this.db = openDatabase('geomood', '1.0', 'Geo-Mood Checkins', 8192);
    this.db.transaction(function(tx) {
      tx.executeSql("create table if not exists " +
        "checkins(id integer primary key asc, time integer, latitude float," +
                  "longitude float, mood string)",
        [],
        function() { console.log("siucc"); }
      );
    });

**Indexed Database** setup takes some work, because it enforces a database version system; if we attempt to open a new database, the result will be a database whose version is null, which is our cue to set it up. And in setting it up, we obviously want to set the version so it doesn't return null next time! Thus, we must call `setVersion()` and we set up the database once the version has been set.

Another thing we do here is creating a mood index, so we will later be able to quickly search for all checkins matching a particular mood.

    setup: function(handler) {

      // attempt to open the database
      var openRequest = indexedDB.open("geomood", "Geo-Mood Checkins");

      // assign the database for access outside
      // the callback and then either upgrade
      // the database if needed or carry on
      openRequest.onsuccess = function(ev) {

        db = ev.target.result;
        db.onerror = function(ev) {
          console.log("db error", arguments, ev.target.webkitErrorMessage);
        };

        if(db.version === version) {
          handler();
        } else {
          indexedStore.reset(handler);
        }
      };
    },

    reset: function(handler) {

      // update the db version
      var versionRequest = db.setVersion(version);

      versionRequest.onsuccess = function(ev) {

        // remove the store if it exists
        if (db.objectStoreNames.contains("checkins")) {
          db.deleteObjectStore("checkins");
        }

        // create a store, and an index
        var checkinsStore = db.createObjectStore("checkins", { keyPath: "time" });
        checkinsStore.createIndex("moodIndex", "mood", { unique: false });

        // now call the handler outside of
        // the 'versionchange' callstack
        var transaction = ev.target.result;
        transaction.oncomplete = function() {
          handler();
        };
      };
    }

Finally, **FileSystem** setup. We'll store each checkin in its own file, JSON-encoded, and all of them inside a "checkins/" directory. Again, this is not the most appropriate use of FileSystem API, but good for demonstration purposes.

The setup gets a handle on the overall FileSystem, using it to check for the "checkins" directory. If it's not there, we create it with getDirectory.

    setup: function(handler) {
      requestFileSystem(
        window.PERSISTENT,
        1024*1024,
        function(fs) {
          fs.root.getDirectory(
            "checkins",
            {}, // no "create" option, so this is a read op
            function(dir) {
              checkinsDir = dir;
              handler();
            },
            function() {
              fs.root.getDirectory(
                "checkins",
                {create: true},
                function(dir) {
                  checkinsDir = dir;
                  handler();
                },
                onError
              );
            }
          );
        },
        function(e) {
          console.log("error "+e.code+"initialising - see http://goo.gl/YW0TI");
        }
      );
    }

### Saving a Checkin

With localStorage, we simply pull the checkins array out, add a new one to the end, and save it again. We also have to do the JSON dance to store it in string form.

    var checkins = JSON.parse(localStorage["checkins"]);
    checkins.push(checkin);
    localStorage["checkins"] = JSON.stringify(checkins);

With Web SQL Database, we run everything inside a transaction. We're going to create a new row in the checkins table, It's a straightforward SQL call, and instead of including the checkin data in the "insert" command, we use "?" syntax because it's cleaner and more secure. The actual data - the four values we want to store as columns in the new checkins row - are specified in the second row. The "?" elements will be replaced by those values (`checkin.time`, `checkin.latitude`, etc.). The next two arguments indicate functions which will be called when the operation has completed, one for success and one for failure. In this app, we use the same generic error handler for all transactions. In this case, the success function is simply the handler that was passed into the search function - we ensure the handler will be called on success so that the UI logic can be notified when the operation has been completed (e.g. to update the count of checkins so far).

    store.db.transaction(function(tx) {
      tx.executeSql(
        "insert into checkins " +
        "(time, latitude, longitude, mood) values (?,?,?,?);",
        [checkin.time, checkin.latitude, checkin.longitude, checkin.mood],
        handler,
        store.onError
      );
    });

Once the store is set up, saving in IndexedDB is almost as simple as Web Storage, with the advantage of working asynchronously, in a transaction:

    var store = db.transaction(["checkins"], 'readwrite').objectStore("checkins");
    var request = store.put(checkin);
    request.onsuccess = handler;

With FileStore, once we create a file and get a handle on it, we can use [the FileWriter API](http://www.w3.org/TR/file-writer-api/) to populate it:

    fs.root.getFile("checkins/" + checkin.time, {create: true, exclusive: true}, function(file) {
      file.createWriter(function(writer) {
        writer.onerror = fileStore.onError;
        var bb = new WebKitBlobBuilder;
        bb.append(JSON.stringify(checkin));
        writer.write(bb.getBlob("text/plain"));
        handler();
      }, fileStore.onError);
    }, fileStore.onError);

### Searching for Matching Checkins

The next function fishes out all checkins matching a particular mood, so the user can see where and when they were happy recently, for example. With localStorage, we have to manually walk through each checkin and compare it to the mood, building up a list of matches. It's good practice to return clones of the data that's stored, rather than the actual objects, since searching should be a read-only operation; hence we pass each matching checkin object through a generic `clone()` operation.

    var allCheckins = JSON.parse(localStorage["checkins"]);
    var matchingCheckins = [];
    allCheckins.forEach(function(checkin) {
      if (checkin.mood == moodQuery) {
        matchingCheckins.push(clone(checkin));
      }
    });
    handler(matchingCheckins);

With Web SQL Database, we perform a query that returns only the checkin rows that we need. However, we still have to manually walk through that list to accumulate the checkin structures, as the database API returns database rows, rather than an array. (This is a good thing for large result sets, but right now, it adds some work for us to do!)

    var matchingCheckins = [];
    store.db.transaction(function(tx) {
      tx.executeSql(
        "select * from checkins where mood=?",
        [moodQuery],
        function(tx, results) {
          for (var i = 0; i < results.rows.length; i++) {
            matchingCheckins.push(clone(results.rows.item(i)));
          }
          handler(matchingCheckins);
        },
        store.onError
      );
    });

Naturally enough, the IndexedDB solution uses an index, the index on "mood we created earlier, called "moodIndex". We use a cursor to iterate through each checkin matching the query. Note that this cursor pattern can also be used against an entire store; so, with indexes, it's like we get a window into the store where we can only see matching objects (similar to a "view" in traditional databases).

    var store = db.transaction(["checkins"], 'readonly').objectStore("checkins");
    var request = moodQuery ?
      store.index("moodIndex").openCursor(new IDBKeyRange.only(moodQuery)) :
      store.openCursor();

    request.onsuccess = function(ev) {
      var cursor = request.result;
      if (cursor) {
        handler(cursor.value);
        cursor["continue"]();
      }
    };

As with many traditional filesystems, there's no indexing, so a search algorithm (like that used by the Unix "grep" command) must iterate through each file. We extract a [Reader](http://www.w3.org/TR/FileAPI/#dfn-filereader) from the checkins directory, which lets us walk through each file via `readEntries()`. For each file, we again extract a reader, and inspect its contents via `readAsText()`. As these operations are asynchronous, we need to chain calls together, which is the function served by `readNext()`.

    checkinsDir.createReader().readEntries(function(files) {
      var reader, fileCount=0, checkins=[];
      var readNextFile = function() {
        reader = new FileReader();
        if (fileCount == files.length) return;
        reader.onload = function(e) {
          var checkin = JSON.parse(this.result);
          if (moodQuery==checkin.mood||moodQuery) handler(checkin);
          readNextFile();
        };
        files[fileCount++].file(function(file) { reader.readAsText(file); });
      };
      readNextFile();
    });

### Counting All Checkins

Finally, we need to count all checkins.

For localStorage, we simply de-serialize the checkins array structure and find its length.

    handler(JSON.parse(localStorage["checkins"]).length);

With Web SQL Database, we could retrieve each row in the database (`select * from checkins`) and look at the length of the result set, but if we know our way around SQL, there's an easier - and faster - way. We can perform a special select statement to retrieve the count. It will return exactly one row, having one column containing the count.

    store.db.transaction(function(tx) {
      tx.executeSql(
        "select count(*) from checkins;",
        [],
        function(tx, results) {
          handler(results.rows.item(0)["count(*)"]);
        },
        store.onError
      );
     }

Unfortunately, Indexed Database doesn't offer any counting facility, so we have to iterate through all checkins.

    var count = 0;
    var request = db.transaction(["checkins"], 'readonly').objectStore("checkins").openCursor();
    request.onsuccess = function(ev) {
      var cursor = request.result;
      cursor ? ++count && cursor["continue"]() : handler(count);
    };

For FileSystem, a directory reader's `readEntries()` method provides a list of files, so we can just return the length of that list.

    checkinsDir.createReader().readEntries(function(files) {
      handler(files.length);
    });

## Summary

This has been a high-level overview of modern client-side storage techniques. You should also check out the [overview on offline apps](http://docs.webplatform.org/wiki/tutorials/about_offline).

## See also

### Related articles

#### Off-line Storage

-   [appcache](/apis/appcache)

-   [status](/apis/appcache/ApplicationCache/status)

-   [file](/apis/file)

-   [File System API](/apis/filesystem)

-   [quota management](/apis/quota_management)

-   [queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)

-   [requestQuota](/apis/quota_management/requestQuota)

-   [localStorage](/apis/web-storage/Storage/localStorage)

-   [Introduction to using the application cache](/tutorials/appcache_beginner)
