{{Page_Title}}
{{Flags}}
{{Summary_Section}}
{{Tutorial
|Content==New Tricks in XMLHttpRequest2=
==By Eric Bidelman==
Published May 27, 2011

==Introduction==

One of the unsung heros in the HTML5 universe is <code>XMLHttpRequest</code>. Strictly speaking XHR2 isn't HTML5. However, it's part of the incremental improvements browser vendors are making to the core platform. I'm including XHR2 in our new bag of goodies because it plays such an integral part in today's complex web apps.

Turns out our old friend got a huge makeover but many folks are unaware of its new features. [http://dev.w3.org/2006/webapi/XMLHttpRequest-2/ XMLHttpRequest Level 2] introduces a slew of new capabilities which put an end to crazy hacks in our web apps; things like cross-origin requests, uploading progress events, and support for uploading/downloading binary data. These allow AJAX to work in concert with many of the bleeding edge HTML5 APIs such as [[tutorials/file_filesystem|File System API]], [http://chromium.googlecode.com/svn/trunk/samples/audio/specification/specification.html Web Audio API], and WebGL.

This tutorial highlights some of the new features in <code>XMLHttpRequest</code>, especially those that can be used for [[tutorials/file_dnd|working with files]].

==Fetching data==

Fetching a file as a binary blob has been painful with XHR. Technically, it wasn't even possible. One trick that has been well documented involves overriding the mime type with a user-defined charset as seen below.

The old way to fetch an image:

 var xhr = new XMLHttpRequest();
 xhr.open('GET', '/path/to/image.png', true);
 
 // Hack to pass bytes through unprocessed.
 '''xhr.overrideMimeType('text/plain; charset=x-user-defined');'''
 
 xhr.onreadystatechange = function(e) {
   if (this.readyState == 4 && this.status == 200) {
     var binStr = this.responseText;
     for (var i = 0, len = binStr.length; i < len; ++i) {
       '''var c = binStr.charCodeAt(i);'''
       '''//String.fromCharCode(c & 0xff);'''
       '''var byte = c & 0xff;  // byte at offset i'''
     }
   }
 };
 
 xhr.send();

While this works, what you actually get back in the <code>responseText</code> is not a binary blob. It is a binary string representing the image file. We're tricking the server into passing the data back, unprocessed. Even though this little gem works, I'm going to call it black magic and advise against it. Anytime you resort to character code hacks and string manipulation for coercing data into a desirable format, that's a problem.

===Specifying a response format===

In the previous example, we downloaded the image as a binary "file" by overriding the server's mime type and processing the response text as a binary string. Instead, let's leverage <code>XMLHttpRequest</code>'s new <code>responseType</code> and <code>response</code> properties to inform the browser what format we want the data returned as.

; xhr.'''responseType'''
;
: Before sending a request, set the <code>xhr.responseType</code> to "text", "arraybuffer", "blob", or "document", depending on your data needs. Note, setting <code><nowiki>xhr.responseType = ''</nowiki></code> (or omitting) will default the response to "text".
; xhr.'''response'''
: After a successful request, the xhr's response property will contain the requested data as a <code>DOMString</code>, <code>ArrayBuffer</code>, <code>Blob</code>, or <code>Document</code> (depending on what was set for <code>responseType</code>.)

With this new awesomeness, we can rework the previous example, but this time, fetch the image as an <code>Blob</code> instead of a string:
 
 var xhr = new XMLHttpRequest();
 xhr.open('GET', '/path/to/image.png', true);
 '''xhr.responseType = 'blob';'''
 
 '''xhr.onload''' = function(e) {
   if (this.status == 200) {
     // Note: .response instead of .responseText
     var blob = new Blob([this.response], {type: 'image/png'});
     ...
   }
 };
 
 xhr.send();

Much nicer!

====ArrayBuffer responses====

An [https://developer.mozilla.org/en/JavaScript_typed_arrays/ArrayBuffer <code>ArrayBuffer</code>] is a generic fixed-length container for binary data. They are super handy if you need a generalized buffer of raw data, but the real power behind these guys is that you can create "views" of the underlying data using [https://developer.mozilla.org/en/JavaScript_typed_arrays JavaScript typed arrays]. In fact, multiple views can be created from a single <code>ArrayBuffer</code> source. For example, you could create an 8-bit integer array that shares the same <code>ArrayBuffer</code> as an existing 32-bit integer array from the same data. The underlying data remains the same, we just create different representations of it.

As an example, the following fetches our same image as an <code>ArrayBuffer</code>, but this time, creates an unsigned 8-bit integer array from that data buffer:
 
 var xhr = new XMLHttpRequest();
 xhr.open('GET', '/path/to/image.png', true);
 '''xhr.responseType = 'arraybuffer';'''
 
 '''xhr.onload''' = function(e) {
   var uInt8Array = new '''Uint8Array'''('''this.response'''); // this.response == uInt8Array.buffer
   // var byte3 = uInt8Array[4]; // byte at offset 4
   ...
 };
 
 xhr.send();

====Blob responses====

If you want to work directly with a [https://developer.mozilla.org/en/DOM/Blob <code>Blob</code>] and/or don't need to manipulate any of the file's bytes, use <code>xhr.responseType='blob'</code><nowiki>:</nowiki>
 
 window.URL = window.URL {{!}}{{!}} window.webkitURL;  // Take care of vendor prefixes.
 
 var xhr = new XMLHttpRequest();
 xhr.open('GET', '/path/to/image.png', true);
 '''xhr.responseType = 'blob';'''
 
 '''xhr.onload''' = function(e) {
   if (this.status == 200) {
     var blob = '''this.response'''<nowiki>;
 
     var img = document.createElement('img');
     img.onload = function(e) {
       </nowiki>'''window.URL.revokeObjectURL(img.src);''' // Clean up after yourself.
     };
     img.src = '''window.URL.createObjectURL(blob);'''
     document.body.appendChild(img);
     ...
   }
 };
 
 xhr.send();

A <code>Blob</code> can be used in a number of places, including writing it to the HTML5 [[tutorials/file_filesystem|File System]], or [[tutorials/workers_basics#BlobURLs|creating a Blob URL]], as seen in this example.

==Sending data==

Being able to download data in different formats is great, but it doesn't get us anywhere if we can't send these rich formats back to home base (the server). <code>XMLHttpRequest</code> has limited us to sending <code>DOMString</code> or <code>Document</code> (XML) data for some time. Not anymore. A revamped <code>send()</code> method has been overridden to accept any of the following types: <code>DOMString</code>, <code>Document</code>, <code>FormData</code>, <code>Blob</code>, <code>File</code>, <code>ArrayBuffer</code>. The examples in the rest of this section demonstrate sending data using each type.

===Sending string data: xhr.send(DOMString)===
 
 function sendText(txt) {
   var xhr = new XMLHttpRequest();
   xhr.open('POST', '/server', true);
   xhr.onload = function(e) {
     if (this.status == 200) {
       console.log('''this.responseText''');
     }
   };
 
   xhr.send(txt);
 }
 
 sendText(''''test string'''');

 
 function sendTextNew(txt) {
   var xhr = new XMLHttpRequest();
   xhr.open('POST', '/server', true);
   '''xhr.responseType = 'text';'''
   xhr.onload = function(e) {
     if (this.status == 200) {
       console.log('''this.response''');
     }
   };
   xhr.send(txt);
 }
 
 sendTextNew(''''test string'''');

There's nothing new here, though the right snippet is slightly different. It sets <code>responseType='text'</code> for comparison. Again, omitting that line yields the same results.

===Submitting forms: xhr.send(FormData)===

Many people are probably accustomed to using [http://jquery.malsup.com/form/ jQuery plugins] or other libraries to handle AJAX form submissions. Instead, we can use [https://developer.mozilla.org/en/XMLHttpRequest/FormData <code>FormData</code>], another new data type conceived for XHR2. <code>FormData</code> is convenient for creating an HTML <code><form></code> on-the-fly, in JavaScript. That form can then be submitted using AJAX:
 
 function sendForm() {
   var formData = new '''FormData'''();
   '''formData.append'''('username', 'johndoe');
   '''formData.append'''('id', 123456);
 
   var xhr = new XMLHttpRequest();
   xhr.open('POST', '/server', true);
   xhr.onload = function(e) { ... };
 
   xhr.send('''formData''');
 }

Essentially, we're just dynamically creating a <code><form></code> and tacking on <code><input></code> values to it by calling the append method.

Of course, you don't need to create a <code><form></code> from scratch. <code>FormData</code> objects can be initialized from and existing <code>HTMLFormElement</code> on the page. For example:
 
 <form id="myform" name="myform" action="/server">
   <input type="text" name="username" value="johndoe">
   <input type="number" name="id" value="123456">
   <input type="submit" onclick="'''return sendForm(this.form);'''">
 </form>
 
 function sendForm(form) {
   var formData = new '''FormData'''(form);
 
   '''formData.append'''('secret_token', '1234567890'); // Append extra data before send.
 
   var xhr = new XMLHttpRequest();
   xhr.open('POST', form.action, true);
   xhr.onload = function(e) { ... };
 
   xhr.send('''formData''');
 
   return false; // Prevent page from submitting.
 }

An HTML form can include file uploads (e.g. <code><input type="file"></code>) and <code>FormData</code> can handle that too. Simply append the file(s) and the browser will construct a <code>multipart/form-data</code> request when <code>send()</code> is called:
 
 function uploadFiles(url, files) {
   var formData = new '''FormData'''();
 
   for (var i = 0, file; file = files[i]; ++i) {
     '''formData.append(file.name, file);'''
   }
 
   var xhr = new XMLHttpRequest();
   xhr.open('POST', url, true);
   xhr.onload = function(e) { ... };
 
   xhr.send('''formData''');  // multipart/form-data
 }
 
 document.querySelector('input[type="file"]').addEventListener('change', function(e) {
   uploadFiles('/server', this.files);
 }, false);

===Uploading a file or blob: xhr.send(Blob)===

We can also send <code>File</code> or <code>Blob</code> data using XHR. Keep in mind all <code>File</code>s are <code>Blob</code>s, so either works here.

This example creates a new text file from scratch using the <code>Blob()</code> constructor and uploads that <code>Blob</code> to the server. The code also sets up a handler to inform the user of the upload's progress:
 
 <progress min="0" max="100" value="0">0% complete</progress>
 
 function upload(blobOrFile) {
   var xhr = new XMLHttpRequest();
   xhr.open('POST', '/server', true);
   xhr.onload = function(e) { ... };
 
   // Listen to the upload progress.
   var progressBar = document.querySelector('progress');
   '''xhr.upload.onprogress''' = function(e) {
     if (e.lengthComputable) {
       progressBar.value = (e.loaded / e.total) * 100;
       progressBar.textContent = progressBar.value; // Fallback for unsupported browsers.
     }
   };
 
   xhr.send('''blobOrFile''');
 }
 
 upload('''new Blob(['hello world'], {type: 'text/plain'})''');

===Uploading a chunk of bytes: xhr.send(ArrayBuffer)===

Last but not least, we can send <code>ArrayBuffer</code>s as the XHR's payload.
 
 function sendArrayBuffer() {
   var xhr = new XMLHttpRequest();
   xhr.open('POST', '/server', true);
   xhr.onload = function(e) { ... };
 
   '''var uInt8Array = new '''Uint8Array'''([1, 2, 3]);'''
 
   xhr.send('''uInt8Array.buffer''');
 }

==Cross Origin Resource Sharing (CORS)==

[http://dev.w3.org/2006/waf/access-control/ CORS] allows web applications on one domain to make cross domain AJAX requests to another domain. It's dead simple to enable, only requiring a single response header to be sent by the server.

===Enabling CORS requests===

Let's say your application lives on <code>example.com</code> and you want to pull data from <code>www.example2.com</code>. Normally if you tried to make this type of AJAX call, the request would fail and the browser would throw an origin mismatch error. With CORS, <code>www.example2.com</code> can choose to allow requests from <code>example.com</code> by simply adding a header:
 
 Access-Control-Allow-Origin: http://example.com

<code>Access-Control-Allow-Origin</code> can be added to a single resource under a site or across the entire domain. To allow ''any'' domain to make a request to you, set:
 
 Access-Control-Allow-Origin: '''<nowiki>*</nowiki>'''

If a site has enabled CORS on its pages, you can fire up the Developer Tools and you'll see the <code>Access-Control-Allow-Origin</code> in our response:

 [[Image:access_control_header.png.pagespeed.ce.QPR4kHOZ9r.png|Access-Control-Allow-Origin]] <code>Access-Control-Allow-Origin</code> header on html5rocks.com.

Enabling cross-origin requests is easy, so please, please, please [http://enable-cors.org/ enable CORS] if your data is public!

===Making a cross-domain request===

If the server endpoint has enabled CORS, making the cross-origin request is no different than a normal <code>XMLHttpRequest</code> request. For example, here is a request <code>example.com</code> can now make to <code>www.example2.com</code><nowiki>:</nowiki>
 
 var xhr = new XMLHttpRequest();
 xhr.open('GET', 'http://www.example2.com/hello.json');
 xhr.onload = function(e) {
   var data = JSON.parse('''this.response''');
   ...
 }
 xhr.send();

==Practical examples==

===Download + save files to the HTML5 file system===

Let's say you have an image gallery and want to fetch a bunch of images then save them locally using the [[tutorials/file_filesystem|HTML5 File System]]. One way to accomplish this would be to request images as <code>Blob</code>s and write them out using <code>FileWriter</code><nowiki>:</nowiki>
 
 window.requestFileSystem  = window.requestFileSystem {{!}}{{!}} window.webkitRequestFileSystem;
 
 function onError(e) {
   console.log('Error', e);
 }
 
 var xhr = new XMLHttpRequest();
 xhr.open('GET', '/path/to/image.png', true);
 '''xhr.responseType = 'blob';'''
 
 '''xhr.onload''' = function(e) {
 
   '''window.requestFileSystem'''(TEMPORARY, 1024 * 1024, function(fs) {
     fs.root.getFile('image.png', {create: true}, function(fileEntry) {
       fileEntry.createWriter(function(writer) {
 
         writer.onwrite = function(e) { ... };
         writer.onerror = function(e) { ... };
 
         var blob = new Blob(['''xhr.response'''], {type: 'image/png'});
 
         '''writer.write'''(blob);
 
       }, onError);
     }, onError);
   }, onError);
 };
 
 xhr.send();

'''Note:''' to use this code, see [[tutorials/file
_filesystem#Browser_support_&_storage_limitations|Browser support & storage limitations] in the [[tutorials/file_filesystem|Exploring the FileSystem APIs]] tutorial.

===Slicing a file and uploading each portion===

Using the [[tutorials/file_dnd|File APIs]], we can minimize the work to upload a large file. The technique is to slice the upload into multiple chunks, spawn an XHR for each portion, and put the file together on the server. This is similar to how GMail uploads large attachments so quickly. Such a technique could also be used to get around Google App Engine's 32MB http request limit.
 
 function upload(blobOrFile) {
   var xhr = new XMLHttpRequest();
   xhr.open('POST', '/server', true);
   xhr.onload = function(e) { ... };
   xhr.send(blobOrFile);
 }
 
 document.querySelector('input[type="file"]').addEventListener('change', function(e) {
   var blob = this.files[0];
 
   const BYTES_PER_CHUNK = 1024 * 1024; // 1MB chunk sizes.
   const SIZE = blob.size;
 
   var start = 0;
   var end = BYTES_PER_CHUNK;
 
   while(start < SIZE) {
     upload(blob.slice(start, end));
 
     start = end;
     end = start + BYTES_PER_CHUNK;
   }
 }, false);
 
 })();

What is not shown here is the code to reconstruct the file on the server.

'''Try it!'''

==References==

* [http://dev.w3.org/2006/webapi/XMLHttpRequest-2/ XMLHttpRequest Level 2] specification
* [http://dev.w3.org/2006/waf/access-control/ Cross Origin Resource Sharing (CORS)] specification
* [http://www.w3.org/TR/file-upload/ File API] specification
* [http://dev.w3.org/2009/dap/file-system/pub/FileSystem/ FileSystem API] specification

}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}