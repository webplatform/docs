{{Flags}}
{{Summary_Section}}
{{Tutorial
|Content==Reading files in JavaScript using the File APIs=

====original by Eric Bidelman====
====published June 18, 2010====

==Supported browsers (remove)==
<span class="browsers"> <span class="browser opera supported"> <span class="browser_name">Opera</span> <span class="support"> supported </span> </span> <span class="browser ie supported"> <span class="browser_name">IE</span> <span class="support"> supported </span> </span> <span class="browser safari supported"> <span class="browser_name">Safari</span> <span class="support"> supported </span> </span> <span class="browser ff supported"> <span class="browser_name">Firefox</span> <span class="support"> supported </span> </span> <span class="browser chrome supported"> <span class="browser_name">Chrome</span> <span class="support"> supported </span> </span> </span><div class="compatible-block">

==Introduction==

HTML5 finally provides a standard way to interact with local files, via the [http://www.w3.org/TR/file-upload/ File API] specification. As examples of its capabilities, the File API could be used to create a thumbnail preview of images as they're sent to the server, or to allow an app to save a file reference while the user is offline. Additionally, you could use client-side logic to verify that an upload's MIME type matches its file extension or to restrict the size of an upload.

The specification provides several interfaces for accessing files from a local filesystem:

# <code>File</code> - an individual file; provides read-only information such as name, file size, MIME type, and a reference to the file handle.
# <code>FileList</code> - an array-like sequence of <code>File</code> objects. (Think <code>&lt;input type="file" multiple&gt;</code> or dragging a directory of files from the desktop.)
# <code>Blob</code> - Allows for slicing a file into byte ranges.

When used in conjunction with the above data structures, the [http://dev.w3.org/2006/webapi/FileAPI/#filereader-interface <code>FileReader</code>] interface can be used to asynchronously read a file through familiar JavaScript event handling. Thus, it is possible to monitor the progress of a read, catch errors, and determine when a load is complete. In many ways the APIs resemble <code>XMLHttpRequest</code>'s event model.

==Selecting files==

The first thing to do is check that your browser fully supports the File API:

<pre>
 // Check for the various File API support.
 if (window.File &amp;&amp; window.FileReader &amp;&amp; window.FileList &amp;&amp; window.Blob) {
   // Great success! All the File APIs are supported.
 } else {
   alert('The File APIs are not fully supported in this browser.');
 }
</pre>

Of course, if your app will only use some of these APIs, modify this snippet accordingly.

===Using form input for selecting===

The most straightforward way to load a file is to use a standard <code>&lt;input type="file"&gt;</code> element. JavaScript returns the list of selected <code>File</code> objects as a <code>FileList</code>. Here's an example that uses the <code>multiple</code> attribute to allow selecting several files at once:

<pre>
 &lt;input type="file" id="files" name="files[]" multiple /&gt;
 &lt;output id="list"&gt;&lt;/output&gt;
 
 &lt;script&gt;
   function handleFileSelect(evt) {
     var files = evt.target.files; // FileList object
 
     // files is a FileList of File objects. List some properties.
     var output = [];
     for (var i = 0, f; f = files[i]; i++) {
       output.push('&lt;li&gt;&lt;strong&gt;', escape(f.name), '&lt;/strong&gt; (', f.type || 'n/a', ') - ',
                   f.size, ' bytes, last modified: ',
                   f.lastModifiedDate ? f.lastModifiedDate.toLocaleDateString() : 'n/a',
                   '&lt;/li&gt;');
     }
     document.getElementById('list').innerHTML = '&lt;ul&gt;' + output.join('') + '&lt;/ul&gt;';
   }
 
   document.getElementById('files').addEventListener('change', handleFileSelect, false);
 &lt;/script&gt;
</pre>

'''Example''': Using form input for selecting. Try it [http://www.html5rocks.com/en/tutorials/file/dndfiles/ here]!

===Using drag and drop for selecting===

Another technique for loading files is native drag and drop from the desktop to the browser. We can modify the previous example slightly to include drag and drop support.

<pre>
 &lt;div id="drop_zone"&gt;Drop files here&lt;/div&gt;
 &lt;output id="list"&gt;&lt;/output&gt;
 
 &lt;script&gt;
   function handleFileSelect(evt) {
     evt.stopPropagation();
     evt.preventDefault();
 
     var files = evt.dataTransfer.files; // FileList object.
 
     // files is a FileList of File objects. List some properties.
     var output = [];
     for (var i = 0, f; f = files[i]; i++) {
       output.push('&lt;li&gt;&lt;strong&gt;', escape(f.name), '&lt;/strong&gt; (', f.type || 'n/a', ') - ',
                   f.size, ' bytes, last modified: ',
                   f.lastModifiedDate ? f.lastModifiedDate.toLocaleDateString() : 'n/a',
                   '&lt;/li&gt;');
     }
     document.getElementById('list').innerHTML = '&lt;ul&gt;' + output.join('') + '&lt;/ul&gt;';
   }
 
   function handleDragOver(evt) {
     evt.stopPropagation();
     evt.preventDefault();
     evt.dataTransfer.dropEffect = 'copy'; // Explicitly show this is a copy.
   }
 
   // Setup the dnd listeners.
   var dropZone = document.getElementById('drop_zone');
   dropZone.addEventListener('dragover', handleDragOver, false);
   dropZone.addEventListener('drop', handleFileSelect, false);
 &lt;/script&gt;
</pre>

'''Example''': Using drag and drop for selecting. Try it[http://www.html5rocks.com/en/tutorials/file/dndfiles/ here]!

'''Note:''' Some browsers treat <code>&lt;input type="file"&gt;</code> elements as native drop targets. Try dragging files onto the input field in the previous example.

==Reading files==

Now comes the fun part!

After you've obtained a <code>File</code> reference, instantiate a [http://dev.w3.org/2006/webapi/FileAPI/#filereader-interface <code>FileReader</code>] object to read its contents into memory. When the load finishes, the reader's <code>onload</code> event is fired and its <code>result</code> attribute can be used to access the file data.

<code>FileReader</code> includes four options for reading a file, asynchronously:

* <code>FileReader.readAsBinaryString(Blob-File)</code> - The <code>result</code> property will contain the file/blob's data as a binary string. Every byte is represented by an integer in the range [0..255].
* <code>FileReader.readAsText(Blob|File, opt_encoding)</code> - The <code>result</code> property will contain the file/blob's data as a text string. By default the string is decoded as 'UTF-8'. Use the optional encoding parameter can specify a different format.
* <code>FileReader.readAsDataURL(Blob|File)</code> - The <code>result</code> property will contain the file/blob's data encoded as a [http://en.wikipedia.org/wiki/Data_URI_scheme data URL].
* <code>FileReader.readAsArrayBuffer(Blob|File)</code> - The <code>result</code> property will contain the file/blob's data as an [https://cvs.khronos.org/svn/repos/registry/trunk/public/webgl/doc/spec/TypedArray-spec.html ArrayBuffer] object.

Once one of these read methods is called on your <code>FileReader</code> object, the <code>onloadstart</code>, <code>onprogress</code>, <code>onload</code>, <code>onabort</code>, <code>onerror</code>, and <code>onloadend</code> events can be used to track its progress.

The example below filters out images from the user's selection, calls <code>reader.readAsDataURL()</code> on the file, and renders a thumbnail by setting the 'src' attribute to a data URL.

<pre>
 &lt;style&gt;
   .thumb {
     height: 75px;
     border: 1px solid #000;
     margin: 10px 5px 0 0;
   }
 &lt;/style&gt;
 
 &lt;input type="file" id="files" name="files[]" multiple /&gt;
 &lt;output id="list"&gt;&lt;/output&gt;
 
 &lt;script&gt;
   function handleFileSelect(evt) {
     var files = evt.target.files; // FileList object
 
     // Loop through the FileList and render image files as thumbnails.
     for (var i = 0, f; f = files[i]; i++) {
 
       // Only process image files.
       if (!f.type.match('image.*')) {
         continue;
       }
 
       var reader = new FileReader();
 
       // Closure to capture the file information.
       reader.onload = (function(theFile) {
         return function(e) {
           // Render thumbnail.
           var span = document.createElement('span');
           span.innerHTML = ['&lt;img class="thumb" src="', e.target.result,
                             '" title="', escape(theFile.name), '"/&gt;'].join('');
           document.getElementById('list').insertBefore(span, null);
         };
       })(f);
 
       // Read in the image file as a data URL.
       reader.readAsDataURL(f);
     }
   }
 
   document.getElementById('files').addEventListener('change', handleFileSelect, false);
 &lt;/script&gt;
</pre>

'''Example''': Reading files. Try it!

<div class="example">
<p>Try this example with a directory of images!</p>
<input type="file" id="files3" name="files3[]" multiple /><br>
<output id="thumbnails"></output>
</div>

===Slicing a file===

In some cases reading the entire file into memory isn't the best option. For example, say you wanted to write an asynchronous file uploader. One possible way to speed up the upload would be to read and send the file in separate byte range chunks. The server component would then be responsible for reconstructing the file content in the correct order.

Luckily for us, the <code>File</code> interface supports a slice method to support this use case. The method takes a starting byte as its first argument, an ending byte as its second, and an optional content type string as a third.

<pre> 
 var blob = file.slice(<var>startingByte</var>, <var>endindByte</var>);
 reader.readAsBinaryString(blob);
</pre>

The following example demonstrates reading chunks of a file. Something worth noting is that it uses the <code>onloadend</code> and checks the <code>evt.target.readyState</code> instead of using the <code>onload</code> event.

<pre>
 &lt;style&gt;
   #byte_content {
     margin: 5px 0;
     max-height: 100px;
     overflow-y: auto;
     overflow-x: hidden;
   }
   #byte_range { margin-top: 5px; }
 &lt;/style&gt;
 
 &lt;input type="file" id="files" name="file" /&gt; Read bytes:
 &lt;span class="readBytesButtons"&gt;
   &lt;button data-startbyte="0" data-endbyte="4"&gt;1-5&lt;/button&gt;
   &lt;button data-startbyte="5" data-endbyte="14"&gt;6-15&lt;/button&gt;
   &lt;button data-startbyte="6" data-endbyte="7"&gt;7-8&lt;/button&gt;
   &lt;button&gt;entire file&lt;/button&gt;
 &lt;/span&gt;
 &lt;div id="byte_range"&gt;&lt;/div&gt;
 &lt;div id="byte_content"&gt;&lt;/div&gt;
 
 &lt;script&gt;
   function readBlob(opt_startByte, opt_stopByte) {
 
     var files = document.getElementById('files').files;
     if (!files.length) {
       alert('Please select a file!');
       return;
     }
 
     var file = files[0];
     var start = parseInt(opt_startByte) || 0;
     var stop = parseInt(opt_stopByte) || file.size - 1;
 
     var reader = new FileReader();
 
     // If we use onloadend, we need to check the readyState.
     reader.onloadend = function(evt) {
       if (evt.target.readyState == FileReader.DONE) { // DONE == 2
         document.getElementById('byte_content').textContent = evt.target.result;
         document.getElementById('byte_range').textContent =
             ['Read bytes: ', start + 1, ' - ', stop + 1,
              ' of ', file.size, ' byte file'].join('');
       }
     };
 
     var blob = file.slice(start, stop + 1);
     reader.readAsBinaryString(blob);
   }
 
   document.querySelector('.readBytesButtons').addEventListener('click', function(evt) {
     if (evt.target.tagName.toLowerCase() == 'button') {
       var startByte = evt.target.getAttribute('data-startbyte');
       var endByte = evt.target.getAttribute('data-endbyte');
       readBlob(startByte, endByte);
     }
   }, false);
 &lt;/script&gt;
</pre>

'''Example''': Slicing a file. Try it!

<div class="example">
<input type="file" id="file4" name="file4"/> Read bytes:
<span class="readBytesButtons">
<button data-startbyte="0" data-endbyte="4">1-5</button>
<button data-startbyte="5" data-endbyte="14">6-15</button>
<button data-startbyte="6" data-endbyte="7">7-8</button>
<button>entire file</button>
</span>
<div id="byte_range"></div>
<div id="byte_content"></div>
</div>

===Monitoring the progress of a read===

One of the nice things that we get for free when using async event handling is the ability to monitor the progress of the file read; useful for large files, catching errors, and figuring out when a read is complete. The <code>onloadstart</code> and <code>onprogress</code> events can be used to monitor the progress of a read.

The example below demonstrates displaying a progress bar to monitor the status of a read. To see the progress indicator in action, try a large file or one from a remote drive.

<pre>
 &lt;style&gt;
   #progress_bar {
     margin: 10px 0;
     padding: 3px;
     border: 1px solid #000;
     font-size: 14px;
     clear: both;
     opacity: 0;
     -moz-transition: opacity 1s linear;
     -o-transition: opacity 1s linear;
     -webkit-transition: opacity 1s linear;
   }
   #progress_bar.loading {
     opacity: 1.0;
   }
   #progress_bar .percent {
     background-color: #99ccff;
     height: auto;
     width: 0;
   }
 &lt;/style&gt;
 
 &lt;input type="file" id="files" name="file" /&gt;
 &lt;button onclick="abortRead();"&gt;Cancel read&lt;/button&gt;
 &lt;div id="progress_bar"&gt;&lt;div class="percent"&gt;0%&lt;/div&gt;&lt;/div&gt;
 
 &lt;script&gt;
   var reader;
   var progress = document.querySelector('.percent');
 
   function abortRead() {
     reader.abort();
   }
 
   function errorHandler(evt) {
     switch(evt.target.error.code) {
       case evt.target.error.NOT_FOUND_ERR:
         alert('File Not Found!');
         break;
       case evt.target.error.NOT_READABLE_ERR:
         alert('File is not readable');
         break;
       case evt.target.error.ABORT_ERR:
         break; // noop
       default:
         alert('An error occurred reading this file.');
     };
   }
 
   function updateProgress(evt) {
     // evt is an ProgressEvent.
     if (evt.lengthComputable) {
       var percentLoaded = Math.round((evt.loaded / evt.total) * 100);
       // Increase the progress bar length.
       if (percentLoaded &lt; 100) {
         progress.style.width = percentLoaded + '%';
         progress.textContent = percentLoaded + '%';
       }
     }
   }
 
   function handleFileSelect(evt) {
     // Reset progress indicator on new file selection.
     progress.style.width = '0%';
     progress.textContent = '0%';
 
     reader = new FileReader();
     reader.onerror = errorHandler;
     reader.onprogress = updateProgress;
     reader.onabort = function(e) {
       alert('File read cancelled');
     };
     reader.onloadstart = function(e) {
       document.getElementById('progress_bar').className = 'loading';
     };
     reader.onload = function(e) {
       // Ensure that the progress bar displays 100% at the end.
       progress.style.width = '100%';
       progress.textContent = '100%';
       setTimeout("document.getElementById('progress_bar').className='';", 2000);
     }
 
     // Read in the image file as a binary string.
     reader.readAsBinaryString(evt.target.files[0]);
   }
 
   document.getElementById('files').addEventListener('change', handleFileSelect, false);
 &lt;/script&gt;
</pre>

'''Example''': Monitoring the progress of a read. Try it!

<div class="example">
<input type="file" id="file5" name="file5"/>
<button onclick="example5.abortRead();">Cancel read</button>
<div id="progress_bar"><div class="percent">0%</div></div>
<p><strong>Tip</strong>: To really see this progress indicator in action, try a large file or a resource on a remote drive.</p>
</div>

==References==

* [http://www.w3.org/TR/file-upload/ File] API specification
* [http://www.w3.org/TR/file-upload/#dfn-filereader FileReader] interface specification
* [http://www.w3.org/TR/file-upload/#dfn-Blob Blob] interface specification
* [http://www.w3.org/TR/file-upload/#dfn-fileerror FileError] interface specification
* [http://www.w3.org/TR/progress-events/#Progress ProgressEvent] specification

Except as otherwise [http://code.google.com/policies.html#restrictions noted], the content of this page is licensed under the [http://creativecommons.org/licenses/by/3.0/ Creative Commons Attribution 3.0 License], and code samples are licensed under the [http://www.apache.org/licenses/LICENSE-2.0 Apache 2.0 License].

|</nowiki>File)</code> - The <code>result</code> property will contain the file/blob's data as an [https://cvs_khronos_org/svn/repos/registry/trunk/public/webgl/doc/spec/TypedArray-spec_html ArrayBuffer] object_

Once one of these read methods is called on your <code>FileReader</code> object, the <code>onloadstart</code>, <code>onprogress</code>, <code>onload</code>, <code>onabort</code>, <code>onerror</code>, and <code>onloadend</code> events can be used to track its progress_

The example below filters out images from the user's selection, calls <code>reader_readAsDataURL()</code> on the file, and renders a thumbnail by setting the 'src' attribute to a data URL_

<pre>
 &lt;style&gt;
   _thumb {
     height: 75px;
     border: 1px solid #000;
     margin: 10px 5px 0 0;
   }
 &lt;/style&gt;
 
 &lt;input type="file" id="files" name="files[]" multiple /&gt;
 &lt;output id="list"&gt;&lt;/output&gt;
 
 &lt;script&gt;
   function handleFileSelect(evt) {
     var files = evt.target.files; // FileList object
 
     // Loop through the FileList and render image files as thumbnails.
     for (var i = 0, f; f = files[i]; i++) {
 
       // Only process image files.
       if (!f.type.match('image.*')) {
         continue;
       }
 
       var reader = new FileReader();
 
       // Closure to capture the file information.
       reader.onload = (function(theFile) {
         return function(e) {
           // Render thumbnail.
           var span = document.createElement('span');
           span.innerHTML = ['&lt;img class="thumb" src="', e.target.result,
                             '" title="', escape(theFile.name), '"/&gt;'].join('');
           document.getElementById('list').insertBefore(span, null);
         };
       })(f);
 
       // Read in the image file as a data URL.
       reader.readAsDataURL(f);
     }
   }
 
   document.getElementById('files').addEventListener('change', handleFileSelect, false);
 &lt;/script&gt;
</pre>

'''Example''': Reading files. Try it!

<div class="example">
<p>Try this example with a directory of images!</p>
<input type="file" id="files3" name="files3[]" multiple /><br>
<output id="thumbnails"></output>
</div>

===Slicing a file===

In some cases reading the entire file into memory isn't the best option. For example, say you wanted to write an asynchronous file uploader. One possible way to speed up the upload would be to read and send the file in separate byte range chunks. The server component would then be responsible for reconstructing the file content in the correct order.

Luckily for us, the <code>File</code> interface supports a slice method to support this use case. The method takes a starting byte as its first argument, an ending byte as its second, and an optional content type string as a third.

<pre> 
 var blob = file.slice(<var>startingByte</var>, <var>endindByte</var>);
 reader.readAsBinaryString(blob);
</pre>

The following example demonstrates reading chunks of a file. Something worth noting is that it uses the <code>onloadend</code> and checks the <code>evt.target.readyState</code> instead of using the <code>onload</code> event.

<pre>
 &lt;style&gt;
   #byte_content {
     margin: 5px 0;
     max-height: 100px;
     overflow-y: auto;
     overflow-x: hidden;
   }
   #byte_range { margin-top: 5px; }
 &lt;/style&gt;
 
 &lt;input type="file" id="files" name="file" /&gt; Read bytes:
 &lt;span class="readBytesButtons"&gt;
   &lt;button data-startbyte="0" data-endbyte="4"&gt;1-5&lt;/button&gt;
   &lt;button data-startbyte="5" data-endbyte="14"&gt;6-15&lt;/button&gt;
   &lt;button data-startbyte="6" data-endbyte="7"&gt;7-8&lt;/button&gt;
   &lt;button&gt;entire file&lt;/button&gt;
 &lt;/span&gt;
 &lt;div id="byte_range"&gt;&lt;/div&gt;
 &lt;div id="byte_content"&gt;&lt;/div&gt;
 
 &lt;script&gt;
   function readBlob(opt_startByte, opt_stopByte) {
 
     var files = document.getElementById('files').files;
     if (!files.length) {
       alert('Please select a file!');
       return;
     }
 
     var file = files[0];
     var start = parseInt(opt_startByte) || 0;
     var stop = parseInt(opt_stopByte) || file.size - 1;
 
     var reader = new FileReader();
 
     // If we use onloadend, we need to check the readyState.
     reader.onloadend = function(evt) {
       if (evt.target.readyState == FileReader.DONE) { // DONE == 2
         document.getElementById('byte_content').textContent = evt.target.result;
         document.getElementById('byte_range').textContent =
             ['Read bytes: ', start + 1, ' - ', stop + 1,
              ' of ', file.size, ' byte file'].join('');
       }
     };
 
     var blob = file.slice(start, stop + 1);
     reader.readAsBinaryString(blob);
   }
 
   document.querySelector('.readBytesButtons').addEventListener('click', function(evt) {
     if (evt.target.tagName.toLowerCase() == 'button') {
       var startByte = evt.target.getAttribute('data-startbyte');
       var endByte = evt.target.getAttribute('data-endbyte');
       readBlob(startByte, endByte);
     }
   }, false);
 &lt;/script&gt;
</pre>

'''Example''': Slicing a file. Try it!

<div class="example">
<input type="file" id="file4" name="file4"/> Read bytes:
<span class="readBytesButtons">
<button data-startbyte="0" data-endbyte="4">1-5</button>
<button data-startbyte="5" data-endbyte="14">6-15</button>
<button data-startbyte="6" data-endbyte="7">7-8</button>
<button>entire file</button>
</span>
<div id="byte_range"></div>
<div id="byte_content"></div>
</div>

===Monitoring the progress of a read===

One of the nice things that we get for free when using async event handling is the ability to monitor the progress of the file read; useful for large files, catching errors, and figuring out when a read is complete. The <code>onloadstart</code> and <code>onprogress</code> events can be used to monitor the progress of a read.

The example below demonstrates displaying a progress bar to monitor the status of a read. To see the progress indicator in action, try a large file or one from a remote drive.

<pre>
 &lt;style&gt;
   #progress_bar {
     margin: 10px 0;
     padding: 3px;
     border: 1px solid #000;
     font-size: 14px;
     clear: both;
     opacity: 0;
     -moz-transition: opacity 1s linear;
     -o-transition: opacity 1s linear;
     -webkit-transition: opacity 1s linear;
   }
   #progress_bar.loading {
     opacity: 1.0;
   }
   #progress_bar .percent {
     background-color: #99ccff;
     height: auto;
     width: 0;
   }
 &lt;/style&gt;
 
 &lt;input type="file" id="files" name="file" /&gt;
 &lt;button onclick="abortRead();"&gt;Cancel read&lt;/button&gt;
 &lt;div id="progress_bar"&gt;&lt;div class="percent"&gt;0%&lt;/div&gt;&lt;/div&gt;
 
 &lt;script&gt;
   var reader;
   var progress = document.querySelector('.percent');
 
   function abortRead() {
     reader.abort();
   }
 
   function errorHandler(evt) {
     switch(evt.target.error.code) {
       case evt.target.error.NOT_FOUND_ERR:
         alert('File Not Found!');
         break;
       case evt.target.error.NOT_READABLE_ERR:
         alert('File is not readable');
         break;
       case evt.target.error.ABORT_ERR:
         break; // noop
       default:
         alert('An error occurred reading this file.');
     };
   }
 
   function updateProgress(evt) {
     // evt is an ProgressEvent.
     if (evt.lengthComputable) {
       var percentLoaded = Math.round((evt.loaded / evt.total) * 100);
       // Increase the progress bar length.
       if (percentLoaded &lt; 100) {
         progress.style.width = percentLoaded + '%';
         progress.textContent = percentLoaded + '%';
       }
     }
   }
 
   function handleFileSelect(evt) {
     // Reset progress indicator on new file selection.
     progress.style.width = '0%';
     progress.textContent = '0%';
 
     reader = new FileReader();
     reader.onerror = errorHandler;
     reader.onprogress = updateProgress;
     reader.onabort = function(e) {
       alert('File read cancelled');
     };
     reader.onloadstart = function(e) {
       document.getElementById('progress_bar').className = 'loading';
     };
     reader.onload = function(e) {
       // Ensure that the progress bar displays 100% at the end.
       progress.style.width = '100%';
       progress.textContent = '100%';
       setTimeout("document.getElementById('progress_bar').className='';", 2000);
     }
 
     // Read in the image file as a binary string.
     reader.readAsBinaryString(evt.target.files[0]);
   }
 
   document.getElementById('files').addEventListener('change', handleFileSelect, false);
 &lt;/script&gt;
</pre>

'''Example''': Monitoring the progress of a read. Try it!

<div class="example">
<input type="file" id="file5" name="file5"/>
<button onclick="example5.abortRead();">Cancel read</button>
<div id="progress_bar"><div class="percent">0%</div></div>
<p><strong>Tip</strong>: To really see this progress indicator in action, try a large file or a resource on a remote drive.</p>
</div>

==References==

* [http://www.w3.org/TR/file-upload/ File] API specification
* [http://www.w3.org/TR/file-upload/#dfn-filereader FileReader] interface specification
* [http://www.w3.org/TR/file-upload/#dfn-Blob Blob] interface specification
* [http://www.w3.org/TR/file-upload/#dfn-fileerror FileError] interface specification
* [http://www.w3.org/TR/progress-events/#Progress ProgressEvent] specification

Except as otherwise [http://code.google.com/policies.html#restrictions noted], the content of this page is licensed under the [http://creativecommons.org/licenses/by/3.0/ Creative Commons Attribution 3.0 License], and code samples are licensed under the [http://www.apache.org/licenses/LICENSE-2.0 Apache 2.0 License].
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