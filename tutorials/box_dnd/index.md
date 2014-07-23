{{Page_Title|Overview of drag and drop download in Chrome}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Flags
}}
{{Byline
|Name=David Tong
|Published=Sept. 25, 2010
}}
{{Summary_Section|An introduction to native drag-and-drop download.}}
{{Tutorial
|Content===Introduction==

Drag and Drop (DnD) is one of the many great features of HTML5. Google recently rolled out a [http://gmailblog.blogspot.com/2010/08/drag-and-drop-attachments-to-save-them.html new feature] that allows Google Chrome users to drag and drop files from the browser to the desktop. It is an extremely convenient feature, but it was not widely known until Ryan Seddon posted an article on the [http://www.thecssninja.com/javascript/gmail-dragout discoveries] of his reverse engineering on this new feature.

At Box.net, we are very excited about how these new capabilities are enabling us to improve our cloud content management solution, as well as contribute more to the developer community. I am pleased to announce that DnD Download has been integrated into our product. Now, Box users can drag files directly from a Chrome browser to their desktop to download and save the file.

I would like to share how I went through several iterations during the development of this new feature.

==Check for Drag and Drop API Support==

The first thing to do is check that your browser fully supports HTML5 drag and drop. An easy way to do that is use a library called [http://www.modernizr.com/ Modernizr] to check for the specific feature:

<pre>
 if (Modernizr.draganddrop) {
   // Browser supports native HTML5 DnD.
 } else {
   // Fallback to a library solution.
 }
</pre>

==Iteration 1==

I first tried the approach that Seddon found in Gmail. I added a new attribute called <code>data-downloadurl</code> to anchor links of files. This process uses HTML5's [http://ejohn.org/blog/html-5-data-attributes/ custom data attributes]. In <code>data-downloadurl</code>, you need to include the MIME type of the file, the destination file name (the desired file name of the downloaded file), and the download URL of the file. Thus, this is added to the HTML template:

<pre>
 &lt;a href="#" class="dnd"
    data-downloadurl="{$item.mime}:{$item.filename}:{$item.url}"&gt;&lt;/a&gt;
</pre>

Which would create an output like this:

<pre>
 &lt;a href="#" class="dnd" data-downloadurl=
   "image/jpeg:Penguins.jpg:https://www.box.net/box_download_file?file_id=f66690"&gt;&lt;/a&gt;
</pre>

Based on a jQuery [http://dev.blog.salesking.eu/coding/jquery-plugin-to-drag-files-from-browser-onto-desktop/ plugin] that von Schorsch created, which is based on Seddon's article, I added a jQuery plugin that does a bit of browser feature detection. Highlighted are the lines that I added to von Schorsch's version:

<pre>
 (function($) {
 
 $.fn.extend({
   dragout: function() {
     var files = this;
     if (files.length &gt; 0) {
       $(files).each(function() {
         var url = (this.dataset &amp;&amp; this.dataset.downloadurl) ||
                    this.getAttribute("data-downloadurl");
         if (this.addEventListener) {
           this.addEventListener("dragstart", function(e) {
             if (e.dataTransfer &amp;&amp; e.dataTransfer.constructor == Clipboard &amp;&amp;
                 e.dataTransfer.setData('DownloadURL', 'http://www.box.net')) {
               e.dataTransfer.setData("DownloadURL", url);
             }
           },false);
         }
       });
     }
   }
 });
 
 })(jQuery);
</pre>

The reason I did this is that without prior browser detection, doing <code>addEventListener()</code> to a HTML element in IE will create a JavaScript error because IE uses its own <code>attachEvent()</code> method. <code>e.dataTransfer</code> is undefined in IE (as of this writing), <code>e.dataTransfer.constructor</code> returns <code>DataTransfer</code> in Firefox (Mozilla), while Webkit browsers (Chrome and Safari) implement the Clipboard constructor. In Safari, <code>e.dataTransfer.setData('DownloadURL','http://www.box.net')</code> returns <code>false</code>, and Chrome returns <code>true</code>. Doing all of the tests mentioned above leaves the feature only available to Chrome. You may argue that I could simply do the following:

<pre>
 /chrome/.test( navigator.userAgent.toLowerCase() )
</pre>

But I prefer feature detection to browser detection, though this technically does not detect that DnD download will work.

===Problems of iteration 1===

1) Because we currently have on-page DnD enabled for moving/copying files between folders, we need a way to distinguish between DnD Download and on-page DnD. Technically, we cannot combine these two actions. We cannot predict whether the user wants to move a file to another folder within the Box.net account or drag it to their desktop, and these two actions are completely different. Moreover, there is no easy way to detect if the cursor is outside the browser window. You could use <code>window.onmouseout</code> (IE) and <code>document.onmouseout</code> (other browsers) to attach a mouseout event to the document, and check if <code>e.relatedTarget.nodeName == 'HTML'</code> (e is the mouseout event or window.event, whichever is available). But this is quite difficult due to event bubbling. The event may trigger randomly when you are over an image or layer, especially in a complex web app like Box.net.

2) We want the user to explicitly do something to prevent them from dragging something out to the desktop by mistake. Potentially, an editor of a Box folder can upload an executable file that does something undesirable on the computer of whoever downloads it. Thus we want the user to know exactly when a file would be downloaded to the desktop.

==Iteration 2==

We decided to experiment with control + drag (dragging a file when the Windows Ctrl key is pressed). This action is consistent with what people can do on a Windows desktop to duplicate a file. It also requires extra work (but not an extra step) from the user to prevent files from being downloaded by mistake.

The jQuery plugin in iteration 1 is abandoned now because we need to tightly integrate DnD Download with the on-page DnD. For those who are interested, we use a modified version of the jQuery UI's [http://jqueryui.com/demos/draggable/ Draggable plugin]. Inside the mousedown event of a target element, we put the following code:

<pre>
 // DnD to desktop when the Ctrl key is pressed while dragging
 if (e.ctrlKey) {
   var that = $(e.target);
   // make sure it is not IE (attachEvent).
   if (that[0].addEventListener) {
       that[0].addEventListener("dragstart",function(e) {
          // e.dataTransfer in Firefox uses the DataTransfer constructor
          // instead of Clipboard
          // make sure it's Chrome and not Safari (both webkit-based).
          // setData on DownloadURL returns true on Chrome, and false on Safari
          if (e.dataTransfer &amp;&amp; e.dataTransfer.constructor == Clipboard &amp;&amp;
              e.dataTransfer.setData('DownloadURL','http://www.box.net')) {
            var url = (this.dataset &amp;&amp; this.dataset.downloadurl) ||
                       this.getAttribute("data-downloadurl");
            e.dataTransfer.setData("DownloadURL", url);
          }
       }, false);
       return;
   }
 }
</pre>

Other than enabling the Ctrl key, we also added a little toaster tooltip, which shows up when the user performs a regular on-page drag. It tells the user that files can be downloaded if the file icon is dragged to the desktop while the Ctrl key is being held.

===Problems of iteration 2===

Due to security concerns, Box.net does not expose permanent URLs to directly access static files. This is not unique to Box.net. Any online storage service should not expose permanent URLs without an extra layer of security to check if the file is public and whether the intended download is requested by a user with appropriate permissions.

When following the download URL (e.g., <code>https://www.box.net/box_download_file?file_id=f_60466690)</code> of an item, it returns a "302 Found" status code, and redirects to a random URL (e.g., <code>https://www.box.net/dl/6045?a=1f1207a084&amp;m=168299,11211&amp;t=2&amp;b=aca15820d924e3b)</code> that is the temporary actual URL of the file. The challenge is that it expires every few minutes, and so placing it in the HTML output is impractical. It could return a "404" when the user tries to download the file at the link in the HTML output generated several minutes ago.

DnD Download only works on actual URLs that point directly to a resource. If redirection is involved, it is currently not smart enough to follow the chain (and it should never follow the chain due to security). Therefore, although the link <code>https://www.box.net/box_download_file?file_id=f_60466690</code> from above would let you download the file when you enter it in the browser location bar, it would not work with DnD.

To better illustrate the differences between an ''actual URL'' and a ''redirect URL'', see the screen shots below:

[[Image:dnd01-redirect.png|302 Redirect URL]]<br/>
''302 redirect URL''

[[Image:dnd02-actualurl.png|Actual URL]]<br/>
''Actual URL''

==Iteration 3==

Let's try Ajax.

We slightly modified the code in the previous iteration and came up with the following:

<pre>
 // DnD to desktop when the Ctrl key is pressed while dragging
 if (e.ctrlKey) {
   var that = $(e.target);
   // make sure it is not IE (attachEvent).
   if (that[0].addEventListener) {
     that[0].addEventListener("dragstart", function(e) {
       // e.dataTransfer in Firefox uses the DataTransfer constructor
       // instead of Clipboard
       // make sure it's Chrome and not Safari (both webkit-based).
       // setData on DownloadURL returns true on Chrome, and false on Safari
       if (e.dataTransfer &amp;&amp; e.dataTransfer.constructor == Clipboard &amp;&amp;
           e.dataTransfer.setData('DownloadURL', 'http://www.box.net')) {
         var url = (this.dataset &amp;&amp; this.dataset.downloadurl) ||
                    this.getAttribute("data-downloadurl");
         $.ajax({
           complete: function(data) {
             e.dataTransfer.setData("DownloadURL", data.responseText);
           },
           type:'GET',
           url: url
         });
       }
     }, false);
     return;
   }
 }
</pre>

This makes sense. Upon dragstart, it immediately makes an Ajax call to the server to retrieve the latest download URL of the file. However, it does not work. It turns out that it needs to be a synchronous call (or as I like to call it, Sjax). Seems like <code>setData</code> has to be done at the time when the event listener is attached. According to jQuery's API, the highlighted lines become:

<pre>
 $.ajax({
   async: false,
   complete: function(data) {
     e.dataTransfer.setData("DownloadURL", data.responseText);
   },
   type: 'GET',
   url: url
 });
</pre>

And it works fine... until I unplugged the network connection. Because it does a synchronous call, the browser freezes until the call is successful. If the Ajax call fails (e.g., with a 404, or if it does not respond at all), the browser would not defrost at all as if it had crashed.

It is much safer to do something like the following:

<pre>
 $.ajax({
   async: false,
   complete: function(data) {
     e.dataTransfer.setData("DownloadURL", data.responseText);
   },
   error: function(xhr) {
     if (xhr.status == 404) {
       xhr.abort();
     }
   },
   type: 'GET',
   timeout: 3000,
   url: url
 });
</pre>

For a demo of this feature, feel free to upload a static file to a Box.net account. Drag the file icon out to your desktop while holding the Ctrl key. If you do not have an account, you can easily createone in less than 30 seconds.

With this feature, you can be creative and make a lot of things possible. Dragging an image to a Windows printer dialog will immediately have the image printed. You can copy a song from Box to your mobile phone's drive, drag a file from Box to your IM client in order to transfer it directly to your friend, etc. This opens up endless possibilities to increase your productivity. See the screen shots below for some examples.

[[Image:dnd03-dragtoprint.png|Dragging a file to the printer]]<br/>
''Dragging a file to the printer''

[[Image:dnd04-dragtoim.png|Dragging a file to an IM client]]<br/>
''Dragging a file to an IM client''

==Thoughts and future improvements==

This is still less than ideal, as a synchronous call could lock up the browser for a brief moment. The HTML5 Web Worker does not help either, as a Web Worker has to be asynchronous. It does seem like <code>setData</code> has to be done at the time when the event listener is attached.

In reality, the performance is pretty acceptable. The synchronous Ajax (Sjax) call merely retrieves a URL string, which should be pretty fast. It does come with big overhead in the HTTP header, which can possibly be addressed by WebSockets. However, until we see more usage of this kind of technology, it is not worth using WebSockets to send every little update down to the client.

I also hope that the capability of multi-file download will be added to the API in the future. Combined with custom checkboxes to select multiple files on the user interface, this would be incredible. Further, it would be even nicer if client-generated files, such as text files generated from the result of a form submitted, could be downloaded in this way.

* Column dnd
* Rearrange list
* Creating an image gallery
* Exporting a canvas image

==References==

* [http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#dnd Drag and Drop] specification
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Drag and Drop
|Chrome_supported=Yes
|Chrome_version=20.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Drag and Drop
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/casestudies/box_dnd_download/
}}