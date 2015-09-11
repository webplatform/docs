---
title: Overview of drag and drop download in Chrome
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/casestudies/box_dnd_download/)'
readiness: 'Ready to Use'
summary: 'An introduction to native drag-and-drop download.'
tags:
  - Tutorials
  - DOM
  - JavaScript
uri: 'tutorials/box dnd'

---
**By David Tong**
Originally published Sept. 25, 2010

## <span>Summary</span>

An introduction to native drag-and-drop download.

## <span>Introduction</span>

Drag and Drop (DnD) is one of the many great features of HTML5. Google recently rolled out a [new feature](http://gmailblog.blogspot.com/2010/08/drag-and-drop-attachments-to-save-them.html) that allows Google Chrome users to drag and drop files from the browser to the desktop. It is an extremely convenient feature, but it was not widely known until Ryan Seddon posted an article on the [discoveries](http://www.thecssninja.com/javascript/gmail-dragout) of his reverse engineering on this new feature.

At Box.net, we are very excited about how these new capabilities are enabling us to improve our cloud content management solution, as well as contribute more to the developer community. I am pleased to announce that DnD Download has been integrated into our product. Now, Box users can drag files directly from a Chrome browser to their desktop to download and save the file.

I would like to share how I went through several iterations during the development of this new feature.

## <span>Check for Drag and Drop API Support</span>

The first thing to do is check that your browser fully supports HTML5 drag and drop. An easy way to do that is use a library called [Modernizr](http://www.modernizr.com/) to check for the specific feature:

     if (Modernizr.draganddrop) {
       // Browser supports native HTML5 DnD.
     } else {
       // Fallback to a library solution.
     }

## <span>Iteration 1</span>

I first tried the approach that Seddon found in Gmail. I added a new attribute called `data-downloadurl` to anchor links of files. This process uses HTML5's [custom data attributes](http://ejohn.org/blog/html-5-data-attributes/). In `data-downloadurl`, you need to include the MIME type of the file, the destination file name (the desired file name of the downloaded file), and the download URL of the file. Thus, this is added to the HTML template:

     <a href="#" class="dnd"
        data-downloadurl="{$item.mime}:{$item.filename}:{$item.url}"></a>

Which would create an output like this:

     <a href="#" class="dnd" data-downloadurl=
       "image/jpeg:Penguins.jpg:https://www.box.net/box_download_file?file_id=f66690"></a>

Based on a jQuery [plugin](http://dev.blog.salesking.eu/coding/jquery-plugin-to-drag-files-from-browser-onto-desktop/) that von Schorsch created, which is based on Seddon's article, I added a jQuery plugin that does a bit of browser feature detection. Highlighted are the lines that I added to von Schorsch's version:

     (function($) {

     $.fn.extend({
       dragout: function() {
         var files = this;
         if (files.length > 0) {
           $(files).each(function() {
             var url = (this.dataset && this.dataset.downloadurl) ||
                        this.getAttribute("data-downloadurl");
             if (this.addEventListener) {
               this.addEventListener("dragstart", function(e) {
                 if (e.dataTransfer && e.dataTransfer.constructor == Clipboard &&
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

The reason I did this is that without prior browser detection, doing `addEventListener()` to a HTML element in IE will create a JavaScript error because IE uses its own `attachEvent()` method. `e.dataTransfer` is undefined in IE (as of this writing), `e.dataTransfer.constructor` returns `DataTransfer` in Firefox (Mozilla), while Webkit browsers (Chrome and Safari) implement the Clipboard constructor. In Safari, `e.dataTransfer.setData('DownloadURL','http://www.box.net')` returns `false`, and Chrome returns `true`. Doing all of the tests mentioned above leaves the feature only available to Chrome. You may argue that I could simply do the following:

     /chrome/.test( navigator.userAgent.toLowerCase() )

But I prefer feature detection to browser detection, though this technically does not detect that DnD download will work.

### <span>Problems of iteration 1</span>

1) Because we currently have on-page DnD enabled for moving/copying files between folders, we need a way to distinguish between DnD Download and on-page DnD. Technically, we cannot combine these two actions. We cannot predict whether the user wants to move a file to another folder within the Box.net account or drag it to their desktop, and these two actions are completely different. Moreover, there is no easy way to detect if the cursor is outside the browser window. You could use `window.onmouseout` (IE) and `document.onmouseout` (other browsers) to attach a mouseout event to the document, and check if `e.relatedTarget.nodeName == 'HTML'` (e is the mouseout event or window.event, whichever is available). But this is quite difficult due to event bubbling. The event may trigger randomly when you are over an image or layer, especially in a complex web app like Box.net.

2) We want the user to explicitly do something to prevent them from dragging something out to the desktop by mistake. Potentially, an editor of a Box folder can upload an executable file that does something undesirable on the computer of whoever downloads it. Thus we want the user to know exactly when a file would be downloaded to the desktop.

## <span>Iteration 2</span>

We decided to experiment with control + drag (dragging a file when the Windows Ctrl key is pressed). This action is consistent with what people can do on a Windows desktop to duplicate a file. It also requires extra work (but not an extra step) from the user to prevent files from being downloaded by mistake.

The jQuery plugin in iteration 1 is abandoned now because we need to tightly integrate DnD Download with the on-page DnD. For those who are interested, we use a modified version of the jQuery UI's [Draggable plugin](http://jqueryui.com/demos/draggable/). Inside the mousedown event of a target element, we put the following code:

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
              if (e.dataTransfer && e.dataTransfer.constructor == Clipboard &&
                  e.dataTransfer.setData('DownloadURL','http://www.box.net')) {
                var url = (this.dataset && this.dataset.downloadurl) ||
                           this.getAttribute("data-downloadurl");
                e.dataTransfer.setData("DownloadURL", url);
              }
           }, false);
           return;
       }
     }

Other than enabling the Ctrl key, we also added a little toaster tooltip, which shows up when the user performs a regular on-page drag. It tells the user that files can be downloaded if the file icon is dragged to the desktop while the Ctrl key is being held.

### <span>Problems of iteration 2</span>

Due to security concerns, Box.net does not expose permanent URLs to directly access static files. This is not unique to Box.net. Any online storage service should not expose permanent URLs without an extra layer of security to check if the file is public and whether the intended download is requested by a user with appropriate permissions.

When following the download URL (e.g., `https://www.box.net/box_download_file?file_id=f_60466690)` of an item, it returns a "302 Found" status code, and redirects to a random URL (e.g., `https://www.box.net/dl/6045?a=1f1207a084&m=168299,11211&t=2&b=aca15820d924e3b)` that is the temporary actual URL of the file. The challenge is that it expires every few minutes, and so placing it in the HTML output is impractical. It could return a "404" when the user tries to download the file at the link in the HTML output generated several minutes ago.

DnD Download only works on actual URLs that point directly to a resource. If redirection is involved, it is currently not smart enough to follow the chain (and it should never follow the chain due to security). Therefore, although the link `https://www.box.net/box_download_file?file_id=f_60466690` from above would let you download the file when you enter it in the browser location bar, it would not work with DnD.

To better illustrate the differences between an *actual URL* and a *redirect URL*, see the screen shots below:

*302 redirect URL* ![302 Redirect URL](/assets/public/2/21/dnd01-redirect.png)

*Actual URL* ![Actual URL](/assets/public/b/b0/dnd02-actualurl.png)

## <span>Iteration 3</span>

Let's try Ajax.

We slightly modified the code in the previous iteration and came up with the following:

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
           if (e.dataTransfer && e.dataTransfer.constructor == Clipboard &&
               e.dataTransfer.setData('DownloadURL', 'http://www.box.net')) {
             var url = (this.dataset && this.dataset.downloadurl) ||
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

This makes sense. Upon dragstart, it immediately makes an Ajax call to the server to retrieve the latest download URL of the file. However, it does not work. It turns out that it needs to be a synchronous call (or as I like to call it, Sjax). Seems like `setData` has to be done at the time when the event listener is attached. According to jQuery's API, the highlighted lines become:

     $.ajax({
       async: false,
       complete: function(data) {
         e.dataTransfer.setData("DownloadURL", data.responseText);
       },
       type: 'GET',
       url: url
     });

And it works fine... until I unplugged the network connection. Because it does a synchronous call, the browser freezes until the call is successful. If the Ajax call fails (e.g., with a 404, or if it does not respond at all), the browser would not defrost at all as if it had crashed.

It is much safer to do something like the following:

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

For a demo of this feature, feel free to upload a static file to a Box.net account. Drag the file icon out to your desktop while holding the Ctrl key. If you do not have an account, you can easily createone in less than 30 seconds.

With this feature, you can be creative and make a lot of things possible. Dragging an image to a Windows printer dialog will immediately have the image printed. You can copy a song from Box to your mobile phone's drive, drag a file from Box to your IM client in order to transfer it directly to your friend, etc. This opens up endless possibilities to increase your productivity. See the screen shots below for some examples.

*Dragging a file to the printer* ![Dragging a file to the printer](/assets/public/1/1f/dnd03-dragtoprint.png)

*Dragging a file to an IM client* ![Dragging a file to an IM client](/assets/public/8/8d/dnd04-dragtoim.png)

## <span>Thoughts and future improvements</span>

This is still less than ideal, as a synchronous call could lock up the browser for a brief moment. The HTML5 Web Worker does not help either, as a Web Worker has to be asynchronous. It does seem like `setData` has to be done at the time when the event listener is attached.

In reality, the performance is pretty acceptable. The synchronous Ajax (Sjax) call merely retrieves a URL string, which should be pretty fast. It does come with big overhead in the HTTP header, which can possibly be addressed by WebSockets. However, until we see more usage of this kind of technology, it is not worth using WebSockets to send every little update down to the client.

I also hope that the capability of multi-file download will be added to the API in the future. Combined with custom checkboxes to select multiple files on the user interface, this would be incredible. Further, it would be even nicer if client-generated files, such as text files generated from the result of a form submitted, could be downloaded in this way.

-   Column dnd
-   Rearrange list
-   Creating an image gallery
-   Exporting a canvas image

## <span>References</span>

-   [Drag and Drop](http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#dnd) specification
