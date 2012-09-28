{{Page_Title}}
{{Flags
|High-level issues=Needs Flags
}}
{{Summary_Section|An introduction to the FileSystem APIs.}}
{{Tutorial
|Content==Exploring the FileSystem APIs=

====original by Eric Bidelman====
====published Jan. 4, 2011, updated Jan. 27, 2012====

==Introduction==

I've always thought it would be handy if web applications could read and write files and directories. As we move from offline to online, applications are becoming more complex and the lack of file system APIs has been a hindrance for moving the web forward. Storing or interacting with binary data shouldn't be limited to the desktop. Thankfully, it no longer is, thanks to the [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/ FileSystem API]. With the FileSystem API, a web app can safely create, read, navigate, and write to a sandboxed section of the user's local file system.

The API is broken up into various themes:

* Reading and manipulating files: <code>File</code>/<code>Blob</code>, <code>FileList</code>, <code>FileReader</code>
* Creating and writing files: <code>Blob()</code>, <code>FileWriter</code>
* Directories and file system access: <code>DirectoryReader</code>, <code>FileEntry</code>/<code>DirectoryEntry</code>, <code>LocalFileSystem</code>

===Browser support & storage limitations===

At the time of this writing, Google Chrome has the only working implementation of the FileSystem API. 
A dedicated browser UI does not yet exist for file/quota management. 
Storing data on the user's system may require your app to [#toc-requesting-quota request quota]. However, for testing, Chrome can be run with the <code>--unlimited-quota-for-files</code> flag. 
Furthermore, if you're building an app or extension for the Chrome Web Store, the <code>unlimitedStorage</code> [http://code.google.com/chrome/extensions/manifest.html manifest file] permission can be used in place of requesting quota. Eventually, users will receive a permission dialog to grant, deny, or increase storage for an app.

You may need the <code>--allow-file-access-from-files</code> flag if you're debugging your app from <code>file://</code>. Not using these flags will result in a <code>SECURITY_ERR</code> or <code>QUOTA_EXCEEDED_ERR</code> FileError.

==Requesting a file system==

A web app can request access to a sandboxed file system by calling <code>window.requestFileSystem()</code>:

<pre>
 // Note: The file system is prefixed in Google Chrome:
 window.requestFileSystem  = window.requestFileSystem &#124;&#124; window.webkitRequestFileSystem;
 
 window.requestFileSystem(type, size, successCallback, opt_errorCallback);
</pre>

The passed parameters are:
; <code>type</code>
: Whether the file storage should be persistent. Possible values are <code>window.TEMPORARY</code> or <code>window.PERSISTENT</code>. Data stored using <code>TEMPORARY</code> can be removed at the browser's discretion (for example if more space is needed). <code>PERSISTENT</code> storage cannot be cleared unless explicitly authorized by the user or the app and requires the user to grant quota to your app. See [#toc-requesting-quota requesting quota].
; <code>size</code>
: Size (in bytes) the app will require for storage.
; <code>successCallback</code>
: Callback that is invoked on successful request of a file system. Its argument is a [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#idl-def-FileSystem <code>FileSystem</code>] object.
; <code>opt_errorCallback</code>
: Optional callback for handling errors or when the request to obtain the file system is denied. Its argument is a [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#idl-def-FileError <code>FileError</code>] object.

If you're calling <code>requestFileSystem()</code> for the first time, new storage is created for your app. It's important to remember that this file system is sandboxed, meaning one web app cannot access another app's files. This also means you cannot read/write files to an arbitrary folder on the user's hard drive (for example My Pictures, My Documents, etc.).

Example usage:

<pre>
 function onInitFs(fs) {
   console.log('Opened file system: ' + fs.name);
 }
 
 window.requestFileSystem(window.TEMPORARY, 5*1024*1024 /*5MB*/, onInitFs, errorHandler);
</pre>

The FileSystem specification also defines a synchronous API <code>[http://dev.w3.org/2009/dap/file-system/file-dir-sys.html#using-localfilesystemsync LocalFileSystemSync]</code> interface that is intended to be used in Web Workers. However, this tutorial will not cover the synchronous API.

Throughout this article, we'll use the same handler for processing errors from the asynchronous calls:

<pre>
 function errorHandler(e) {
   var msg = '';
 
   switch (e.code) {
     case FileError.QUOTA_EXCEEDED_ERR:
       msg = 'QUOTA_EXCEEDED_ERR';
       break;
     case FileError.NOT_FOUND_ERR:
       msg = 'NOT_FOUND_ERR';
       break;
     case FileError.SECURITY_ERR:
       msg = 'SECURITY_ERR';
       break;
     case FileError.INVALID_MODIFICATION_ERR:
       msg = 'INVALID_MODIFICATION_ERR';
       break;
     case FileError.INVALID_STATE_ERR:
       msg = 'INVALID_STATE_ERR';
       break;
     default:
       msg = 'Unknown Error';
       break;
   };
 
   console.log('Error: ' + msg);
 }
</pre>

Granted, this error callback is very generic, but you get the idea. You'll want to provide human-readable messages to users instead.

===Requesting storage quota===

To use <code>PERSISTENT</code> storage, you must obtain permission from the user to store peristent data. The same restriction doesn't apply to <code>TEMPORARY</code> storage because the browser may choose to evict temporarily stored data at its discretion.

To use <code>PERSISTENT</code> storage with the FileSystem API, Chrome exposes a new API under <code>window.webkitStorageInfo</code> to request storage:

<pre>
 window.webkitStorageInfo.requestQuota(PERSISTENT, 1024*1024, function(grantedBytes) {
   window.requestFileSystem(PERSISTENT, grantedBytes, onInitFs, errorHandler);
 }, function(e) {
   console.log('Error', e);
 });
</pre>

Once the user has granted permission, there's no need to call <code>requestQuota()</code> in the future unless you wish to increase your app's quota. Subsequent calls for equal or lesser quota are a no-op.

There is also [https://groups.google.com/a/chromium.org/group/chromium-html5/browse_thread/thread/9be7a2dc04d9af67 an API] to query an origin's current quota usage and allocation: <code>window.webkitStorageInfo.queryUsageAndQuota()</code>.

==Working with files==

Files in the sandboxed environment are represented by the [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#the-fileentry-interface <code>FileEntry</code>] interface. 
A FileEntry contains the types of properties (<code>name</code>, <code>isFile</code>, etc.) and methods (<code>remove</code>, <code>moveTo</code>, <code>copyTo</code>, etc.) that you'd expect from a standard file system.

Properties and methods of <code>FileEntry</code>:

<pre>
 fileEntry.isFile === true
 fileEntry.isDirectory === false
 fileEntry.name
 fileEntry.fullPath
 ...
 
 fileEntry.getMetadata(successCallback, opt_errorCallback);
 fileEntry.remove(successCallback, opt_errorCallback);
 fileEntry.moveTo(dirEntry, opt_newName, opt_successCallback, opt_errorCallback);
 fileEntry.copyTo(dirEntry, opt_newName, opt_successCallback, opt_errorCallback);
 fileEntry.getParent(successCallback, opt_errorCallback);
 fileEntry.toURL(opt_mimeType);
 
 fileEntry.file(successCallback, opt_errorCallback);
 fileEntry.createWriter(successCallback, opt_errorCallback);
 ...
</pre>

To better understand <code>FileEntry</code>, the rest of this section contains a bunch of recipes for performing common tasks.

===Creating a file===

You can look up or create a file with the file system's <code>getFile()</code> method, a method of the DirectoryEntry interface. After requesting a file system, the success callback is passed a <code>FileSystem</code> object that contains a <code>DirectoryEntry</code> (<code>fs.root</code>) pointing to the root of the app's file system.

The following code creates an empty file called "log.txt" in the root of the app's file system:

<pre>
 function onInitFs(fs) {
 
   fs.root.getFile('log.txt', {create: true, exclusive: true}, function(fileEntry) {
 
     // fileEntry.isFile === true
     // fileEntry.name == 'log.txt'
     // fileEntry.fullPath == '/log.txt'
 
   }, errorHandler);
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

Once the file system has been requested, the success handler is passed a <code>FileSystem</code> object. Inside the callback, we can call <code>fs.root.getFile()</code> with the name of the file to create. You can pass an absolute or relative path, but it must be valid. For instance, it is an error to attempt to create a file whose immediate parent does not exist. 

The second argument to <code>getFile()</code> is an object literal describing the function's behavior if the file does not exist. In this example, <code>create: true</code> creates the file if it doesn't exist and throws an error if it does (<code>exclusive: true</code>). Otherwise (if <code>create: false</code>), the file is simply fetched and returned. In either case, the file contents are not overwritten because we're just obtaining a reference entry to the file in question.

===Reading a file by name===

The following code retrieves the file called "log.txt", its contents are read using the <code>FileReader</code> API and appended to a new <textarea> on the page. If log.txt doesn't exist, an error is thrown.

<pre>
 function onInitFs(fs) {
 
   fs.root.getFile('log.txt', {}, function(fileEntry) {
 
     // Get a File object representing the file,
     // then use FileReader to read its contents.
     fileEntry.file(function(file) {
        var reader = new FileReader();
 
        reader.onloadend = function(e) {
          var txtArea = document.createElement('textarea');
          txtArea.value = this.result;
          document.body.appendChild(txtArea);
        };
 
        reader.readAsText(file);
     }, errorHandler);
 
   }, errorHandler);
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

===Writing to a file===

The following code creates an empty file called "log.txt" (if it doesn't exist) and fills it with the text 'Lorem Ipsum'.

<pre>
 function onInitFs(fs) {
 
   fs.root.getFile('log.txt', {create: true}, function(fileEntry) {
 
     // Create a FileWriter object for our FileEntry (log.txt).
     fileEntry.createWriter(function(fileWriter) {
 
       fileWriter.onwriteend = function(e) {
         console.log('Write completed.');
       };
 
       fileWriter.onerror = function(e) {
         console.log('Write failed: ' + e.toString());
       };
 
       // Create a new Blob and write it to log.txt.
       var blob = new Blob(['Lorem Ipsum'], {type: 'text/plain'});
 
       fileWriter.write(blob);
 
     }, errorHandler);
 
   }, errorHandler);
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

This time, we call the FileEntry's <code>createWriter()</code> method to obtain a <code>FileWriter</code> object. Inside the success callback, event handlers are set up for <code>error</code> and <code>writeend</code> events. The text data is written to the file by creating a blob, appending text to it, and passing the blob to <code>FileWriter.write()</code>.

===Appending data to a file===

The following code appends the text "Hello World" to the end of our log file. An error is thrown if the file does not exist.

<pre>
 function onInitFs(fs) {
 
   fs.root.getFile('log.txt', {create: false}, function(fileEntry) {
 
     // Create a FileWriter object for our FileEntry (log.txt).
     fileEntry.createWriter(function(fileWriter) {
 
       fileWriter.seek(fileWriter.length); // Start write position at EOF.
 
       // Create a new Blob and write it to log.txt.
       var blob = new Blob(['Hello World'], {type: 'text/plain'});
 
       fileWriter.write(blob);
 
     }, errorHandler);
 
   }, errorHandler);
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

===Duplicating user-selected files===

The following code allows a user to select multiple files using <code><input type="file" multiple /></code> and creates copies of those files in the app's sandboxed file system.

<pre>
 <input type="file" id="myfile" multiple />
</pre>

<pre>
 document.querySelector('#myfile').onchange = function(e) {
   var files = this.files;
 
   window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
     // Duplicate each file the user selected to the app's fs.
     for (var i = 0, file; file = files[i]; ++i) {
 
       // Capture current iteration's file in local scope for the getFile() callback.
       (function(f) {
         fs.root.getFile(f.name, {create: true, exclusive: true}, function(fileEntry) {
           fileEntry.createWriter(function(fileWriter) {
             fileWriter.write(f); // Note: write() can take a File or Blob object.
           }, errorHandler);
         }, errorHandler);
       })(file);
 
     }
   }, errorHandler);
 
 };
</pre>

Although we've used an input for the file import, one could easily leverage HTML5 Drag and Drop to achieve the same objective.

As noted in the comment, <code>FileWriter.write()</code> can accept a <code>Blob</code> or <code>File</code>. This is because <code>File</code> inherits from <code>Blob</code>. Therefore, all file objects are blobs.

===Removing a file===

The following code deletes the file 'log.txt'.

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getFile('log.txt', {create: false}, function(fileEntry) {
 
     fileEntry.remove(function() { console.log('File removed.'); }, errorHandler);
 
   }, errorHandler);
 }, errorHandler);
</pre>

==Working with directories==

Directories in the sandbox are represented by the [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#the-directoryentry-interface <code>DirectoryEntry</code>] interface, which shares most of FileEntry's properties (they inherit from a common <code>Entry</code> interface). However, <code>DirectoryEntry</code> has additional methods for manipulating directories.

Properties and methods of <code>DirectoryEntry</code>:

<pre>
 dirEntry.isDirectory === true
 // See the section on FileEntry for other inherited properties/methods.
 ...
 
 var dirReader = dirEntry.createReader();
 dirEntry.getFile(path, opt_flags, opt_successCallback, opt_errorCallback);
 dirEntry.getDirectory(path, opt_flags, opt_successCallback, opt_errorCallback);
 dirEntry.removeRecursively(successCallback, opt_errorCallback);
 ...
</pre>

===Creating directories===

Use the <code>getDirectory()</code> method of <code>DirectoryEntry</code> to read or create directories. You can pass either a name or path as the directory to look up or create.

For example, the following code creates a directory named "MyPictures" in the root directory:

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getDirectory('MyPictures', {create: true}, function(dirEntry) {
     ...
   }, errorHandler);
 }, errorHandler);
</pre>

===Subdirectories===

Creating a subdirectory is exactly the same as creating any other directory. However, the API throws an error if you attempt to create a directory whose immediate parent does not exist. The solution is to create each directory sequentially, which is rather tricky to do with an asynchronous API.

The following code creates a new hierarchy ("music/genres/jazz") in the root of the app's FileSystem by recursively adding each subdirectory after its parent folder has been created.

<pre>
 var path = 'music/genres/jazz/';
 
 function createDir(rootDirEntry, folders) {
   // Throw out './' or '/' and move on to prevent something like '/foo/.//bar'.
   if (folders[0] == '.' &#124;&#124; folders[0] == '') {
     folders = folders.slice(1);
   }
   rootDirEntry.getDirectory(folders[0], {create: true}, function(dirEntry) {
     // Recursively add the new subfolder (if we still have another to create).
     if (folders.length) {
       createDir(dirEntry, folders.slice(1));
     }
   }, errorHandler);
 };
 
 function onInitFs(fs) {
   createDir(fs.root, path.split('/')); // fs.root is a DirectoryEntry.
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

Now that "music/genres/jazz" is in place, we can pass its full path to <code>getDirectory()</code> and create new subfolders or files under it. For example:

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getFile('/music/genres/jazz/song.mp3', {create: true}, function(fileEntry) {
     ...
   }, errorHandler);
 }, errorHandler);
</pre>

===Reading a directory's contents===

To read the contents of a directory, create a <code>DirectoryReader</code> and call its <code>readEntries()</code> method. Note that there is no guarantee that all of a directory's entries will be returned in a single call to <code>readEntries()</code>. 
That means you need to keep calling <code>DirectoryReader.readEntries()</code> until no more results are returned. The following code demonstrates this:

<pre>
 <ul id="filelist"></ul>
</pre>

<pre>
 function toArray(list) {
   return Array.prototype.slice.call(list &#124;&#124; [], 0);
 }
 
 function listResults(entries) {
   // Document fragments can improve performance since they're only appended
   // to the DOM once. Only one browser reflow occurs.
   var fragment = document.createDocumentFragment();
 
   entries.forEach(function(entry, i) {
     var img = entry.isDirectory ? '<img src="folder-icon.gif">' :
                                   '<img src="file-icon.gif">';
     var li = document.createElement('li');
     li.innerHTML = [img, '<span>', entry.name, '</span>'].join('');
     fragment.appendChild(li);
   });
 
   document.querySelector('#filelist').appendChild(fragment);
 }
 
 function onInitFs(fs) {
 
   var dirReader = fs.root.createReader();
   var entries = [];
 
   // Call the reader.readEntries() until no more results are returned.
   var readEntries = function() {
      dirReader.readEntries (function(results) {
       if (!results.length) {
         listResults(entries.sort());
       } else {
         entries = entries.concat(toArray(results));
         readEntries();
       }
     }, errorHandler);
   };
 
   readEntries(); // Start reading dirs.
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

===Removing a directory===

The <code>DirectoryEntry.remove()</code> method behaves just like [#toc-file-removing <code>FileEntry</code>]'s. The difference: attempting to delete a non-empty directory results in an error.

The following code removes the empty directory "jazz" from "/music/genres/":

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getDirectory('music/genres/jazz', {}, function(dirEntry) {
 
     dirEntry.remove(function() { console.log('Directory removed.'); }, errorHandler);
 
   }, errorHandler);
 }, errorHandler);
</pre>

====Recursively removing a directory====

If you have a pesky directory that contains entries, <code>removeRecursively()</code> is your friend. It deletes the directory and its contents, recursively.

The following code recursively removes the directory "music" and all the files and directories that it contains:

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getDirectory('/misc/../music', {}, function(dirEntry) {
 
     dirEntry.removeRecursively(function() { console.log('Directory removed.'); }, errorHandler);
 
   }, errorHandler);
 }, errorHandler);
</pre>

==Copying, renaming, and moving==

<code>FileEntry</code> and <code>DirectoryEntry</code> share common operations.

===Copying an entry===

Both <code>FileEntry</code> and <code>DirectoryEntry</code> have a <code>copyTo()</code> method for duplicating existing entries. This method automatically does a recursive copy on folders.

The following code example copies the file "me.png" from one directory to another:

<pre>
 function copy(cwd, src, dest) {
   cwd.getFile(src, {}, function(fileEntry) {
 
     cwd.getDirectory(dest, {}, function(dirEntry) {
       fileEntry.copyTo(dirEntry);
     }, errorHandler);
 
   }, errorHandler);
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   copy(fs.root, '/folder1/me.png', 'folder2/mypics/');
 }, errorHandler);
</pre>

===Moving or renaming an entry===

The <code>moveTo()</code> method present in <code>FileEntry</code> and <code>DirectoryEntry</code> allows you to move or rename a file or directory. Its first argument is the parent directory to move the file under, and its second is an optional new name for the file. If a new name isn't provided, the file's original name is used.

The following example renames "me.png" to "you.png", but does not move the file:

<pre>
 function rename(cwd, src, newName) {
   cwd.getFile(src, {}, function(fileEntry) {
     fileEntry.moveTo(cwd, newName);
   }, errorHandler);
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   rename(fs.root, 'me.png', 'you.png');
 }, errorHandler);
</pre>

The following example moves "me.png" (located in the root directory) to a folder named "newfolder".

<pre>
 function move(src, dirName) {
   fs.root.getFile(src, {}, function(fileEntry) {
 
     fs.root.getDirectory(dirName, {}, function(dirEntry) {
       fileEntry.moveTo(dirEntry);
     }, errorHandler);
 
   }, errorHandler);
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   move('/me.png', 'newfolder/');
 }, errorHandler);
</pre>

==filesystem: URLs==

The FileSystem API exposes a new URL scheme, <code>filesystem:</code>, that can be used to fill <code>src</code> or <code>href</code> attributes. For example, if you wanted to display an image and have its [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#the-fileentry-interface <code>fileEntry</code>], calling <code>toURL()</code> would give you the file's <code>filesystem:</code> URL:

<pre>
 var img = document.createElement('img');
 img.src = fileEntry.toURL(); // filesystem:http://example.com/temporary/myfile.png
 document.body.appendChild(img);
</pre>

Alternatively, if you already have a <code>filesystem:</code> URL, <code>resolveLocalFileSystemURL()</code> will get you back the [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#the-fileentry-interface <code>fileEntry</code>]:

<pre>
 window.resolveLocalFileSystemURL = window.resolveLocalFileSystemURL &#124;&#124;
                                    window.webkitResolveLocalFileSystemURL;
 
 var url = 'filesystem:http://example.com/temporary/myfile.png';
 window.resolveLocalFileSystemURL(url, function(fileEntry) {
   ...
 });
</pre>

==Putting it all together==

===Basic example===

The demo in [http://www.html5rocks.com/en/tutorials/file/filesystem/ this article] will list the files/folders in the filesystem.

===HTML5 Terminal===

The HTML5 Terminal shell replicates some of the common operations in a UNIX filesystem (such as <code>cd</code>, <code>mkdir</code>, <code>rm</code>, <code>open</code>, and <code>cat</code>) by abstracting the FileSystem API. To add content, open the app, then drag and drop files from your desktop onto the terminal window. (Click the image caption to open the terminal.)

[[Image:xterminal2b.jpg]]<br/>
[http://www.htmlfivewow.com/demos/terminal/terminal.html ''Click here to open the HTML5 Terminal'']

==Use Cases==

There are several [http://www.html5rocks.com/tutorials#offline,storage storage options] available in HTML5, but the FileSystem is different in that it aims to satisfy client-side storage use cases not well served by databases. Generally, these are applications that deal with large binary blobs and/or share data with applications outside of the context of the browser.

The specification lists several use cases:

# Persistent uploader
#* When a file or directory is selected for upload, it copies the files into a local sandbox and uploads a chunk at a time.
#* Uploads can be restarted after browser crashes, network interruptions, etc.
# Video game, music, or other app with lots of media assets
#* It downloads one or several large tarballs, and expands them locally into a directory structure.
#* The same download works on any operating system.
#* It can manage prefetching just the next-to-be-needed assets in the background, so going to the next game level or activating a new feature doesn't require waiting for a download.
#* It uses those assets directly from its local cache, by direct file reads or by handing local URIs to image or video tags, WebGL asset loaders, etc.
#* The files may be of arbitrary binary format.
#* On the server side, a compressed tarball will often be much smaller than a collection of separately-compressed files. Also, 1 tarball instead of 1000 little files will involve fewer seeks, all else being equal.
# Audio/Photo editor with offline access or local cache for speed
#* The data blobs are potentially quite large, and are read-write.
#* It may want to do partial writes to files (ovewriting just the ID3/EXIF tags, for example).
#* The ability to organize project files by creating directories would be useful.
#* Edited files should be accessable by client-side applications [iTunes, Picasa].
# Offline video viewer
#* It downloads large files (>1GB) for later viewing.
#* It needs efficient seek + streaming.
#* It must be able to hand a URI to the video tag.
#* It should enable access to partly-downloaded files e.g. to let you watch the first episode of the DVD even if your download didn't complete before you got on the plane.
#* It should be able to pull a single episode out of the middle of a download and give just that to the video tag.
# Offline Web Mail Client
#* Downloads attachments and stores them locally.
#* Caches user-selected attachments for later upload.
#* Needs to be able to refer to cached attachments and image thumbnails for display and upload.
#* Should be able to trigger the UA's download manager just as if talking to a server.
#* Should be able to upload an email with attachments as a multipart post, rather than sending a file at a time in an XHR.

==Reference specifications==

* [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/ FileSystem]
* [http://dev.w3.org/2009/dap/file-system/file-writer.html FileWriter]
* [http://dev.w3.org/2006/webapi/FileAPI/#dfn-filereader FileReader]
* [http://dev.w3.org/2006/webapi/FileAPI/ File]
* [http://dev.w3.org/2006/webapi/FileAPI/#dfn-Blob Blob]
|window_webkitRequestFileSystem;
 
 window_requestFileSystem(type, size, successCallback, opt_errorCallback);
</pre>

The passed parameters are:
; <code>type</code>
: Whether the file storage should be persistent_ Possible values are <code>window_TEMPORARY</code> or <code>window_PERSISTENT</code>_ Data stored using <code>TEMPORARY</code> can be removed at the browser's discretion (for example if more space is needed)_ <code>PERSISTENT</code> storage cannot be cleared unless explicitly authorized by the user or the app and requires the user to grant quota to your app_ See [#toc-requesting-quota requesting quota]_
; <code>size</code>
: Size (in bytes) the app will require for storage_
; <code>successCallback</code>
: Callback that is invoked on successful request of a file system_ Its argument is a [http://dev_w3_org/2009/dap/file-system/pub/FileSystem/#idl-def-FileSystem <code>FileSystem</code>] object_
; <code>opt_errorCallback</code>
: Optional callback for handling errors or when the request to obtain the file system is denied_ Its argument is a [http://dev_w3_org/2009/dap/file-system/pub/FileSystem/#idl-def-FileError <code>FileError</code>] object_

If you're calling <code>requestFileSystem()</code> for the first time, new storage is created for your app_ It's important to remember that this file system is sandboxed, meaning one web app cannot access another app's files_ This also means you cannot read/write files to an arbitrary folder on the user's hard drive (for example My Pictures, My Documents, etc_)_

Example usage:

<pre>
 function onInitFs(fs) {
   console_log('Opened file system: ' + fs_name);
 }
 
 window_requestFileSystem(window_TEMPORARY, 5*1024*1024 /*5MB*/, onInitFs, errorHandler);
</pre>

The FileSystem specification also defines a synchronous API <code>[http://dev_w3_org/2009/dap/file-system/file-dir-sys_html#using-localfilesystemsync LocalFileSystemSync]</code> interface that is intended to be used in Web Workers_ However, this tutorial will not cover the synchronous API_

Throughout this article, we'll use the same handler for processing errors from the asynchronous calls:

<pre>
 function errorHandler(e) {
   var msg='';
 
   switch (e.code) {
     case FileError.QUOTA_EXCEEDED_ERR:
       msg = 'QUOTA_EXCEEDED_ERR';
       break;
     case FileError.NOT_FOUND_ERR:
       msg = 'NOT_FOUND_ERR';
       break;
     case FileError.SECURITY_ERR:
       msg = 'SECURITY_ERR';
       break;
     case FileError.INVALID_MODIFICATION_ERR:
       msg = 'INVALID_MODIFICATION_ERR';
       break;
     case FileError.INVALID_STATE_ERR:
       msg = 'INVALID_STATE_ERR';
       break;
     default:
       msg = 'Unknown Error';
       break;
   };
 
   console.log('Error: ' + msg);
 }
</pre>

Granted, this error callback is very generic, but you get the idea. You'll want to provide human-readable messages to users instead.

===Requesting storage quota===

To use <code>PERSISTENT</code> storage, you must obtain permission from the user to store peristent data. The same restriction doesn't apply to <code>TEMPORARY</code> storage because the browser may choose to evict temporarily stored data at its discretion.

To use <code>PERSISTENT</code> storage with the FileSystem API, Chrome exposes a new API under <code>window.webkitStorageInfo</code> to request storage:

<pre>
 window.webkitStorageInfo.requestQuota(PERSISTENT, 1024*1024, function(grantedBytes) {
   window.requestFileSystem(PERSISTENT, grantedBytes, onInitFs, errorHandler);
 }, function(e) {
   console.log('Error', e);
 });
</pre>

Once the user has granted permission, there's no need to call <code>requestQuota()</code> in the future unless you wish to increase your app's quota. Subsequent calls for equal or lesser quota are a no-op.

There is also [https://groups.google.com/a/chromium.org/group/chromium-html5/browse_thread/thread/9be7a2dc04d9af67 an API] to query an origin's current quota usage and allocation: <code>window.webkitStorageInfo.queryUsageAndQuota()</code>.

==Working with files==

Files in the sandboxed environment are represented by the [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#the-fileentry-interface <code>FileEntry</code>] interface. 
A FileEntry contains the types of properties (<code>name</code>, <code>isFile</code>, etc.) and methods (<code>remove</code>, <code>moveTo</code>, <code>copyTo</code>, etc.) that you'd expect from a standard file system.

Properties and methods of <code>FileEntry</code>:

<pre>
 fileEntry.isFile === true
 fileEntry.isDirectory === false
 fileEntry.name
 fileEntry.fullPath
 ...
 
 fileEntry.getMetadata(successCallback, opt_errorCallback);
 fileEntry.remove(successCallback, opt_errorCallback);
 fileEntry.moveTo(dirEntry, opt_newName, opt_successCallback, opt_errorCallback);
 fileEntry.copyTo(dirEntry, opt_newName, opt_successCallback, opt_errorCallback);
 fileEntry.getParent(successCallback, opt_errorCallback);
 fileEntry.toURL(opt_mimeType);
 
 fileEntry.file(successCallback, opt_errorCallback);
 fileEntry.createWriter(successCallback, opt_errorCallback);
 ...
</pre>

To better understand <code>FileEntry</code>, the rest of this section contains a bunch of recipes for performing common tasks.

===Creating a file===

You can look up or create a file with the file system's <code>getFile()</code> method, a method of the DirectoryEntry interface. After requesting a file system, the success callback is passed a <code>FileSystem</code> object that contains a <code>DirectoryEntry</code> (<code>fs.root</code>) pointing to the root of the app's file system.

The following code creates an empty file called "log.txt" in the root of the app's file system:

<pre>
 function onInitFs(fs) {
 
   fs.root.getFile('log.txt', {create: true, exclusive: true}, function(fileEntry) {
 
     // fileEntry.isFile === true
     // fileEntry.name == 'log.txt'
     // fileEntry.fullPath == '/log.txt'
 
   }, errorHandler);
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

Once the file system has been requested, the success handler is passed a <code>FileSystem</code> object. Inside the callback, we can call <code>fs.root.getFile()</code> with the name of the file to create. You can pass an absolute or relative path, but it must be valid. For instance, it is an error to attempt to create a file whose immediate parent does not exist. 

The second argument to <code>getFile()</code> is an object literal describing the function's behavior if the file does not exist. In this example, <code>create: true</code> creates the file if it doesn't exist and throws an error if it does (<code>exclusive: true</code>). Otherwise (if <code>create: false</code>), the file is simply fetched and returned. In either case, the file contents are not overwritten because we're just obtaining a reference entry to the file in question.

===Reading a file by name===

The following code retrieves the file called "log.txt", its contents are read using the <code>FileReader</code> API and appended to a new <textarea> on the page. If log.txt doesn't exist, an error is thrown.

<pre>
 function onInitFs(fs) {
 
   fs.root.getFile('log.txt', {}, function(fileEntry) {
 
     // Get a File object representing the file,
     // then use FileReader to read its contents.
     fileEntry.file(function(file) {
        var reader = new FileReader();
 
        reader.onloadend = function(e) {
          var txtArea = document.createElement('textarea');
          txtArea.value = this.result;
          document.body.appendChild(txtArea);
        };
 
        reader.readAsText(file);
     }, errorHandler);
 
   }, errorHandler);
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

===Writing to a file===

The following code creates an empty file called "log.txt" (if it doesn't exist) and fills it with the text 'Lorem Ipsum'.

<pre>
 function onInitFs(fs) {
 
   fs.root.getFile('log.txt', {create: true}, function(fileEntry) {
 
     // Create a FileWriter object for our FileEntry (log.txt).
     fileEntry.createWriter(function(fileWriter) {
 
       fileWriter.onwriteend = function(e) {
         console.log('Write completed.');
       };
 
       fileWriter.onerror = function(e) {
         console.log('Write failed: ' + e.toString());
       };
 
       // Create a new Blob and write it to log.txt.
       var blob = new Blob(['Lorem Ipsum'], {type: 'text/plain'});
 
       fileWriter.write(blob);
 
     }, errorHandler);
 
   }, errorHandler);
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

This time, we call the FileEntry's <code>createWriter()</code> method to obtain a <code>FileWriter</code> object. Inside the success callback, event handlers are set up for <code>error</code> and <code>writeend</code> events. The text data is written to the file by creating a blob, appending text to it, and passing the blob to <code>FileWriter.write()</code>.

===Appending data to a file===

The following code appends the text "Hello World" to the end of our log file. An error is thrown if the file does not exist.

<pre>
 function onInitFs(fs) {
 
   fs.root.getFile('log.txt', {create: false}, function(fileEntry) {
 
     // Create a FileWriter object for our FileEntry (log.txt).
     fileEntry.createWriter(function(fileWriter) {
 
       fileWriter.seek(fileWriter.length); // Start write position at EOF.
 
       // Create a new Blob and write it to log.txt.
       var blob = new Blob(['Hello World'], {type: 'text/plain'});
 
       fileWriter.write(blob);
 
     }, errorHandler);
 
   }, errorHandler);
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

===Duplicating user-selected files===

The following code allows a user to select multiple files using <code><input type="file" multiple /></code> and creates copies of those files in the app's sandboxed file system.

<pre>
 <input type="file" id="myfile" multiple />
</pre>

<pre>
 document.querySelector('#myfile').onchange = function(e) {
   var files = this.files;
 
   window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
     // Duplicate each file the user selected to the app's fs.
     for (var i = 0, file; file = files[i]; ++i) {
 
       // Capture current iteration's file in local scope for the getFile() callback.
       (function(f) {
         fs.root.getFile(f.name, {create: true, exclusive: true}, function(fileEntry) {
           fileEntry.createWriter(function(fileWriter) {
             fileWriter.write(f); // Note: write() can take a File or Blob object.
           }, errorHandler);
         }, errorHandler);
       })(file);
 
     }
   }, errorHandler);
 
 };
</pre>

Although we've used an input for the file import, one could easily leverage HTML5 Drag and Drop to achieve the same objective.

As noted in the comment, <code>FileWriter.write()</code> can accept a <code>Blob</code> or <code>File</code>. This is because <code>File</code> inherits from <code>Blob</code>. Therefore, all file objects are blobs.

===Removing a file===

The following code deletes the file 'log.txt'.

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getFile('log.txt', {create: false}, function(fileEntry) {
 
     fileEntry.remove(function() { console.log('File removed.'); }, errorHandler);
 
   }, errorHandler);
 }, errorHandler);
</pre>

==Working with directories==

Directories in the sandbox are represented by the [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#the-directoryentry-interface <code>DirectoryEntry</code>] interface, which shares most of FileEntry's properties (they inherit from a common <code>Entry</code> interface). However, <code>DirectoryEntry</code> has additional methods for manipulating directories.

Properties and methods of <code>DirectoryEntry</code>:

<pre>
 dirEntry.isDirectory === true
 // See the section on FileEntry for other inherited properties/methods.
 ...
 
 var dirReader = dirEntry.createReader();
 dirEntry.getFile(path, opt_flags, opt_successCallback, opt_errorCallback);
 dirEntry.getDirectory(path, opt_flags, opt_successCallback, opt_errorCallback);
 dirEntry.removeRecursively(successCallback, opt_errorCallback);
 ...
</pre>

===Creating directories===

Use the <code>getDirectory()</code> method of <code>DirectoryEntry</code> to read or create directories. You can pass either a name or path as the directory to look up or create.

For example, the following code creates a directory named "MyPictures" in the root directory:

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getDirectory('MyPictures', {create: true}, function(dirEntry) {
     ...
   }, errorHandler);
 }, errorHandler);
</pre>

===Subdirectories===

Creating a subdirectory is exactly the same as creating any other directory. However, the API throws an error if you attempt to create a directory whose immediate parent does not exist. The solution is to create each directory sequentially, which is rather tricky to do with an asynchronous API.

The following code creates a new hierarchy ("music/genres/jazz") in the root of the app's FileSystem by recursively adding each subdirectory after its parent folder has been created.

<pre>
 var path = 'music/genres/jazz/';
 
 function createDir(rootDirEntry, folders) {
   // Throw out './' or '/' and move on to prevent something like '/foo/.//bar'.
   if (folders[0] == '.' || folders[0] == '') {
     folders = folders.slice(1);
   }
   rootDirEntry.getDirectory(folders[0], {create: true}, function(dirEntry) {
     // Recursively add the new subfolder (if we still have another to create).
     if (folders.length) {
       createDir(dirEntry, folders.slice(1));
     }
   }, errorHandler);
 };
 
 function onInitFs(fs) {
   createDir(fs.root, path.split('/')); // fs.root is a DirectoryEntry.
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

Now that "music/genres/jazz" is in place, we can pass its full path to <code>getDirectory()</code> and create new subfolders or files under it. For example:

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getFile('/music/genres/jazz/song.mp3', {create: true}, function(fileEntry) {
     ...
   }, errorHandler);
 }, errorHandler);
</pre>

===Reading a directory's contents===

To read the contents of a directory, create a <code>DirectoryReader</code> and call its <code>readEntries()</code> method. Note that there is no guarantee that all of a directory's entries will be returned in a single call to <code>readEntries()</code>. 
That means you need to keep calling <code>DirectoryReader.readEntries()</code> until no more results are returned. The following code demonstrates this:

<pre>
 <ul id="filelist"></ul>
</pre>

<pre>
 function toArray(list) {
   return Array.prototype.slice.call(list || [], 0);
 }
 
 function listResults(entries) {
   // Document fragments can improve performance since they're only appended
   // to the DOM once. Only one browser reflow occurs.
   var fragment = document.createDocumentFragment();
 
   entries.forEach(function(entry, i) {
     var img = entry.isDirectory ? '<img src="folder-icon.gif">' :
                                   '<img src="file-icon.gif">';
     var li = document.createElement('li');
     li.innerHTML = [img, '<span>', entry.name, '</span>'].join('');
     fragment.appendChild(li);
   });
 
   document.querySelector('#filelist').appendChild(fragment);
 }
 
 function onInitFs(fs) {
 
   var dirReader = fs.root.createReader();
   var entries = [];
 
   // Call the reader.readEntries() until no more results are returned.
   var readEntries = function() {
      dirReader.readEntries (function(results) {
       if (!results.length) {
         listResults(entries.sort());
       } else {
         entries = entries.concat(toArray(results));
         readEntries();
       }
     }, errorHandler);
   };
 
   readEntries(); // Start reading dirs.
 
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, onInitFs, errorHandler);
</pre>

===Removing a directory===

The <code>DirectoryEntry.remove()</code> method behaves just like [#toc-file-removing <code>FileEntry</code>]'s. The difference: attempting to delete a non-empty directory results in an error.

The following code removes the empty directory "jazz" from "/music/genres/":

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getDirectory('music/genres/jazz', {}, function(dirEntry) {
 
     dirEntry.remove(function() { console.log('Directory removed.'); }, errorHandler);
 
   }, errorHandler);
 }, errorHandler);
</pre>

====Recursively removing a directory====

If you have a pesky directory that contains entries, <code>removeRecursively()</code> is your friend. It deletes the directory and its contents, recursively.

The following code recursively removes the directory "music" and all the files and directories that it contains:

<pre>
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   fs.root.getDirectory('/misc/../music', {}, function(dirEntry) {
 
     dirEntry.removeRecursively(function() { console.log('Directory removed.'); }, errorHandler);
 
   }, errorHandler);
 }, errorHandler);
</pre>

==Copying, renaming, and moving==

<code>FileEntry</code> and <code>DirectoryEntry</code> share common operations.

===Copying an entry===

Both <code>FileEntry</code> and <code>DirectoryEntry</code> have a <code>copyTo()</code> method for duplicating existing entries. This method automatically does a recursive copy on folders.

The following code example copies the file "me.png" from one directory to another:

<pre>
 function copy(cwd, src, dest) {
   cwd.getFile(src, {}, function(fileEntry) {
 
     cwd.getDirectory(dest, {}, function(dirEntry) {
       fileEntry.copyTo(dirEntry);
     }, errorHandler);
 
   }, errorHandler);
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   copy(fs.root, '/folder1/me.png', 'folder2/mypics/');
 }, errorHandler);
</pre>

===Moving or renaming an entry===

The <code>moveTo()</code> method present in <code>FileEntry</code> and <code>DirectoryEntry</code> allows you to move or rename a file or directory. Its first argument is the parent directory to move the file under, and its second is an optional new name for the file. If a new name isn't provided, the file's original name is used.

The following example renames "me.png" to "you.png", but does not move the file:

<pre>
 function rename(cwd, src, newName) {
   cwd.getFile(src, {}, function(fileEntry) {
     fileEntry.moveTo(cwd, newName);
   }, errorHandler);
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   rename(fs.root, 'me.png', 'you.png');
 }, errorHandler);
</pre>

The following example moves "me.png" (located in the root directory) to a folder named "newfolder".

<pre>
 function move(src, dirName) {
   fs.root.getFile(src, {}, function(fileEntry) {
 
     fs.root.getDirectory(dirName, {}, function(dirEntry) {
       fileEntry.moveTo(dirEntry);
     }, errorHandler);
 
   }, errorHandler);
 }
 
 window.requestFileSystem(window.TEMPORARY, 1024*1024, function(fs) {
   move('/me.png', 'newfolder/');
 }, errorHandler);
</pre>

==filesystem: URLs==

The FileSystem API exposes a new URL scheme, <code>filesystem:</code>, that can be used to fill <code>src</code> or <code>href</code> attributes. For example, if you wanted to display an image and have its [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#the-fileentry-interface <code>fileEntry</code>], calling <code>toURL()</code> would give you the file's <code>filesystem:</code> URL:

<pre>
 var img = document.createElement('img');
 img.src = fileEntry.toURL(); // filesystem:http://example.com/temporary/myfile.png
 document.body.appendChild(img);
</pre>

Alternatively, if you already have a <code>filesystem:</code> URL, <code>resolveLocalFileSystemURL()</code> will get you back the [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/#the-fileentry-interface <code>fileEntry</code>]:

<pre>
 window.resolveLocalFileSystemURL = window.resolveLocalFileSystemURL {{!}}{{!}}
                                    window.webkitResolveLocalFileSystemURL;
 
 var url = 'filesystem:http://example.com/temporary/myfile.png';
 window.resolveLocalFileSystemURL(url, function(fileEntry) {
   ...
 });
</pre>

==Putting it all together==

===Basic example===

The demo in [http://www.html5rocks.com/en/tutorials/file/filesystem/ this article] will list the files/folders in the filesystem.

===HTML5 Terminal===

The HTML5 Terminal shell replicates some of the common operations in a UNIX filesystem (such as <code>cd</code>, <code>mkdir</code>, <code>rm</code>, <code>open</code>, and <code>cat</code>) by abstracting the FileSystem API. To add content, open the app, then drag and drop files from your desktop onto the terminal window. (Click the image caption to open the terminal.)

[[Image:xterminal2.jpg]]<br/>
[http://www.htmlfivewow.com/demos/terminal/terminal.html ''Click here to open the HTML5 Terminal'']

==Use Cases==

There are several [http://www.html5rocks.com/tutorials#offline,storage storage options] available in HTML5, but the FileSystem is different in that it aims to satisfy client-side storage use cases not well served by databases. Generally, these are applications that deal with large binary blobs and/or share data with applications outside of the context of the browser.

The specification lists several use cases:

# Persistent uploader
#* When a file or directory is selected for upload, it copies the files into a local sandbox and uploads a chunk at a time.
#* Uploads can be restarted after browser crashes, network interruptions, etc.
# Video game, music, or other app with lots of media assets
#* It downloads one or several large tarballs, and expands them locally into a directory structure.
#* The same download works on any operating system.
#* It can manage prefetching just the next-to-be-needed assets in the background, so going to the next game level or activating a new feature doesn't require waiting for a download.
#* It uses those assets directly from its local cache, by direct file reads or by handing local URIs to image or video tags, WebGL asset loaders, etc.
#* The files may be of arbitrary binary format.
#* On the server side, a compressed tarball will often be much smaller than a collection of separately-compressed files. Also, 1 tarball instead of 1000 little files will involve fewer seeks, all else being equal.
# Audio/Photo editor with offline access or local cache for speed
#* The data blobs are potentially quite large, and are read-write.
#* It may want to do partial writes to files (ovewriting just the ID3/EXIF tags, for example).
#* The ability to organize project files by creating directories would be useful.
#* Edited files should be accessable by client-side applications [iTunes, Picasa].
# Offline video viewer
#* It downloads large files (>1GB) for later viewing.
#* It needs efficient seek + streaming.
#* It must be able to hand a URI to the video tag.
#* It should enable access to partly-downloaded files e.g. to let you watch the first episode of the DVD even if your download didn't complete before you got on the plane.
#* It should be able to pull a single episode out of the middle of a download and give just that to the video tag.
# Offline Web Mail Client
#* Downloads attachments and stores them locally.
#* Caches user-selected attachments for later upload.
#* Needs to be able to refer to cached attachments and image thumbnails for display and upload.
#* Should be able to trigger the UA's download manager just as if talking to a server.
#* Should be able to upload an email with attachments as a multipart post, rather than sending a file at a time in an XHR.

==Reference specifications==

* [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/ FileSystem]
* [http://dev.w3.org/2009/dap/file-system/file-writer.html FileWriter]
* [http://dev.w3.org/2006/webapi/FileAPI/#dfn-filereader FileReader]
* [http://dev.w3.org/2006/webapi/FileAPI/ File]
* [http://dev.w3.org/2006/webapi/FileAPI/#dfn-Blob Blob]
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Filesystem API
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=20.0
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Filesystem API
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|FileAPI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/file/filesystem/
}}