{{Page_Title|New Tricks in XMLHttpRequest2}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Eric Bidelman
|URL=http://www.html5rocks.com/profiles/#ericbidelman
|Published=May 27, 2011, updated Aug. 21, 2012
}}
{{Summary_Section|A guide to using the XMLHttpRequest2 API.}}
{{Tutorial
|Content=<h2 id="toc-introduction">Introduction</h2>

One of the unsung heros in the HTML5 universe is <code>XMLHttpRequest</code>. Strictly speaking XHR2 isn't HTML5. However, it's part of the incremental improvements browser vendors are making to the core platform. I'm including XHR2 in our new bag of goodies because it plays such an integral part in today's complex web apps.

Turns out our old friend got a huge makeover but many folks are unaware of its new features. [http://dev.w3.org/2006/webapi/XMLHttpRequest-2/ XMLHttpRequest Level 2] introduces a slew of new capabilities which put an end to crazy hacks in our web apps; things like cross-origin requests, uploading progress events, and support for uploading/downloading binary data. These allow AJAX to work in concert with many of the bleeding edge HTML5 APIs such as [[tutorials/file_filesystem|File System API]], [http://chromium.googlecode.com/svn/trunk/samples/audio/specification/specification.html Web Audio API], and WebGL.

This tutorial highlights some of the new features in <code>XMLHttpRequest</code>, especially those that can be used for [[tutorials/file_dnd|working with files]].

<h2 id="toc-bin-data">Fetching data</h2>

Fetching a file as a binary blob has been painful with XHR. Technically, it wasn't even possible. One trick that has been well documented involves overriding the mime type with a user-defined charset as seen below.

<p id="toc-old-download">The old way to fetch an image:</p>

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

<h3 id="toc-response">Specifying a response format</h3>

In the previous example, we downloaded the image as a binary "file" by overriding the server's mime type and processing the response text as a binary string. Instead, let's leverage <code>XMLHttpRequest</code>'s new <code>responseType</code> and <code>response</code> properties to inform the browser what format we want the data returned as.

; xhr.'''responseType'''
: Before sending a request, set the <code>xhr.responseType</code> to "text", "arraybuffer", "blob", or "document", depending on your data needs. Note, setting <code>xhr.responseType = ''</code> (or omitting) will default the response to "text".
; xhr.'''response'''
: After a successful request, the xhr's response property will contain the requested data as a <code>DOMString</code>, <code>ArrayBuffer</code>, <code>Blob</code>, or <code>Document</code> (depending on what was set for <code>responseType</code>.)

With this new awesomeness, we can rework the previous example, but this time, fetch the image as an <code>Blob</code> instead of a string:

<pre>
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
</pre>

Much nicer!
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=XMLHttpRequest2
|Chrome_supported=Yes
|Chrome_version=20
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=XMLHttpRequest2
|Android_supported=Yes
|Android_version=3.0
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
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|FileAPI, IndexedDB, Webworkers, XHR}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/file/xhr2/
}}