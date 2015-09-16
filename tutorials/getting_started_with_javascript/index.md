---
title: Getting started with JavaScript
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Getting_Started)'
notes:
  - 'Needs some content, fix broken links'
readiness: 'In Progress'
summary: 'This tutorial provides a brief introduction to JavaScript, for readers who are already familiar with programming concepts'
tags:
  - Tutorials
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'tutorials/getting started with javascript/DOM/event/keypress'
    - 'tutorials/getting started with javascript/DOM/event.charCode'
uri: 'tutorials/getting started with javascript'

---
## Summary

This tutorial provides a brief introduction to JavaScript, for readers who are already familiar with programming concepts

## Why JavaScript?

JavaScript is a powerful, complicated and not very well understood language in the field of computer languages. However, at its core potential lies the ability to develop a new range of applications that will likely change the landscape of the internet in this decade. A good example of one of these applications is [Google Maps](http://local.google.com/).

The primary advantage to JavaScript, which is also known as ECMAScript, centers around the web browser, thus having the ability to produce the same results on all platforms supported by the browser. The examples on this page, just like Google Maps, run on Linux, Windows and the Mac OS. With the recent growth of numerous JavaScript libraries, it is now easier to navigate a document, select DOM elements, create animations, handle events, and develop Ajax applications. Unlike the hype around other technologies pushed by various proprietary interests, JavaScript is really the only cross-platform, client-side programming language that is both free and universally adopted.

## What you should already know

JavaScript is a very easy language to start programming with. All you need is a text editor and a web browser to get started.

There are many other technologies that can be integrated into and developed along with JavaScript that are beyond the scope of this document. Don't expect to make a whole application like Google maps all on your first day!

## Getting Started

Getting started with JavaScript is very easy. You don't have to have complicated development programs installed. You don't have to know how to use a shell, program Make or use a compiler. JavaScript is interpreted by your web browser. All you have to do is save your program as a text file and then open it up in your web browser. That's it!

JavaScript is a great programming language for introductory computer courses. It allows instant feedback to the new student and teaches them about tools they will likely find useful in their real life. This is in stark contrast to C, C++ and Java which are really only useful for dedicated software developers.

## Browser Compatibility Issues

There are variations between what functionality is available in the different browsers. Mozilla, Microsoft IE, Apple Safari and Opera fluctuate in the behavior. We intend on documenting these variations. You can mitigate these issues by using the various cross platform JavaScript APIs that are available. These APIs provide common functionality and hide these browser fluctuations from you.

## How to try the Examples

The examples below have some sample code. There are many ways to try these examples out. If you already have your own website, then you should be able to just save these examples as new web pages on your website.

If you do not have your own website, you can save these examples as files on your computer and open them up with the web browser you are using now. JavaScript is a very easy language to use for beginning programmers for this reason. You don't need a compiler or a development environment; you and your browser are all you need to get started!

## Example: Catching a mouse click

The specifics of event handling (event types, handler registration, propagation, etc) are too extensive to be fully covered in this simple example. However this example cannot demonstrate catching a mouse click without delving a little into the JavaScript event system. Just keep in mind that this example will only graze the full details about JavaScript events and that if you wish to go beyond the basic capabilities described here to read more about the JavaScript event system.

'Mouse' events are a subset of the total events issued by a web browser in response to user actions. The following is a list of the the events emitted in response to a user's mouse action:

-   Click - issued when a user clicks the mouse
-   DblClick - issued when a user double-clicks the mouse
-   MouseDown - issued when a user depresses a mouse button (the first half of a click)
-   MouseUp - issued when a user releases a mouse button (the second half of a click)
-   MouseOut - issued when the mouse pointer leaves the graphical bounds of the object
-   MouseOver - issued when the mouse pointer enters the graphical bounds of the object
-   MouseMove - issued when the mouse pointer moves while within the graphical bounds of the object
-   ContextMenu - issued when the user clicks using the right mouse button

The simplest method for capturing these events, to register event handlers — using HTML — is to specify the individual events as attributes for your element. Example:

      <span onclick="alert('Hello World!');">Click Here</span>

The JavaScript code you wish to execute can be inlined as the attribute value or you can call a function which has been defined in a `<script>` block within the HTML page:

``` html
 <script type="text/javascript">;
   function onclick_callback () {
      alert ("Hello, World!");
   }
 </script>
 <span onclick="onclick_callback();">Click Here</span>;
```

Additionally, the event object which is issued can be captured and referenced; providing the developer with access to specifics about the event such as which object received the event, the event's type, and which mouse button was clicked. Using the inline example again:

``` html
 <script type="text/javascript">
   function onclick_callback(event) {
     var eType = event.type;
     /* the following is for compatability */
     /* Moz populates the target property of the event object */
     /* IE populates the srcElement property */
     var eTarget = event.target || event.srcElement;

     alert( "Captured Event (type=" + eType + ", target=" + eTarget );
   }
 </script>
 <span onclick="onclick_callback(event);">Click Here</span>
```

In addition to registering to receive events in your HTML you can likewise set the same attributes of any HTMLElement objects generated by your JavaScript. The example below instantiates a span object, appends it to the page body, and registers the span object to recieve mouse-over, mouse-out, mouse-down, and mouse-up events.

``` html
 <script type="text/javascript">
   function mouseevent_callback(event) {
     /* The following is for compatability */
     /* IE does NOT by default pass the event object */
     /* obtain a ref to the event if one was not given */
     if (!event) event = window.event;

     /* obtain event type and target as earlier */
     var eType = event.type;
     var eTarget = event.target || event.srcElement;
     alert(eType +' event on element with id: '+ eTarget.id);
   }

  function myloadevent () {
    /* obtain a ref to the 'body' element of the page */
    var body = document.body;
    /* create a span element to be clicked */
    var span = document.createElement('span');
    span.id = 'ExampleSpan';
    span.appendChild(document.createTextNode ('Click Here!'));

    /* register the span object to receive specific mouse events */
    span.onmousedown = mouseevent_callback;
    span.onmouseup = mouseevent_callback;
    span.onmouseover = mouseevent_callback;
    span.onmouseout = mouseevent_callback;

    /* display the span on the page */
    body.appendChild(span);
 }
 </script>
```

**DRAFT**
<font size="x-small">This page is not complete.</font>

## Example: Catching a keyboard event

Similar to the "Catching a mouse event" example above, catching a keyboard event relies on exploring the JavaScript event system. Keyboard events are fired whenever any key is used on the keyboard.

The list of available keyboard events emitted in response to a keyboard action is considerably smaller than those available for mouse:

-   KeyPress - issued when a key is depressed and released
-   KeyDown - issued when a key is depressed but hasn't yet been released
-   KeyUp - issued when a key is released
-   TextInput (available in Webkit browsers only at time of writing) - issued when text is input either by pasting, speaking or keyboard. This event will not be covered in this article.

In a [keypress](/w/index.php?title=tutorials/getting_started_with_javascript/DOM/event/keypress&action=edit&redlink=1) event, the Unicode value of the key pressed is stored in either the `keyCode` or `charCode` property; never both. If the key pressed generates a character (e.g. 'a'), `charCode` is set to the code of that character, respecting the letter case. (i.e. `charCode` takes into account whether the shift key is held down). Otherwise, the code of the pressed key is stored in `keyCode`.

The simplest method for capturing keyboard events is again to register event handlers within the HTML, specifying the individual events as attributes for your element. Example:

``` html
   <input type="text" onkeypress="alert ('Hello World!');"></input>
```

As with mouse events, the JavaScript code you wish to execute can be inlined as the attribute value or you can call a function which has been defined in a &lt;script\> block within the HTML page:

``` html
 <script type="text/javascript">
   function onkeypress_callback () {
     alert ("Hello, World!");
   }
 </script>

 <input onkeypress="onkeypress_callback();"></input>
```

Capturing the event and referencing the target (i.e. the actual key that was pressed) is achieved in a similar way to mouse events:

``` html
 <script type="text/javascript">
   function onkeypress_callback(evt) {
       var eType = evt.type; // Will return "keypress" as the event type
       var eCode = 'keyCode is ' + evt.keyCode;
       var eChar = 'charCode is ' + evt.charCode;

       alert ("Captured Event (type=" + eType + ", key Unicode value=" + eCode + ", ASCII value=" + eChar + ")");
    }
 </script>
 <input onkeypress="onkeypress_callback(event);"></input>
```

Capturing any key event from the page can be done by registering the event at the document level and handling it in a function:

``` html
 <script type="text/javascript">
   document.onkeypress = key_event(event);
   document.onkeydown = key_event(event);
   document.onkeyup = key_event(event)

   function key_event(evt) {
       var eType = evt.type;
       var eCode = "ASCII code is " + evt.keyCode;
       var eChar = 'charCode is ' + evt.charCode;

       alert ("Captured Event (type=" + eType + ", key Unicode value=" + eCode + ", ASCII value=" + eChar + ")");
    }
 </script>
```

Here is a complete example that shows key event handling:

``` html
 <!DOCTYPE html>
 <html>
 <head>
   <script>
     var metaChar = false;
     var exampleKey = 16;
     function keyEvent(event) {
       var key = event.keyCode || event.which;
       var keychar = String.fromCharCode(key);
       if (key==exampleKey) { metaChar = true; }
       if (key!=exampleKey) {
          if (metaChar) {
             alert("Combination of metaKey + " + keychar)
             metaChar = false;
          } else { alert("Key pressed " + key); }
       }
     }
     function metaKeyUp (event) {
       var key = event.keyCode || event.which;
       if (key==exampleKey) { metaChar = false; }
     }
   </script>
 </head>
 <body onkeydown="keyEvent(event)" onkeyup="metaKeyUp(event)">
 </body>
 </html>
```

### Browser bugs and quirks

The two properties made available through the key events are `keyCode` and `charCode`. In simple terms, `keyCode` refers to the actual keyboard key that was pressed by the user, while `charCode` is intended to return that key's ASCII value. These two values may not necessarily be the same; for instance, a lower case 'a' and an upper case 'A' have the same `keyCode`, because the user presses the same key, but a different `charCode` because the resulting character is different.

The way in which browsers interpret the charCode is not a consistently-applied process. For example, Internet Explorer and Opera do not support `charCode`. However, they give the character information in `keyCode`, but only onkeypress. Onkeydown and -up `keyCode` contains key information. Firefox uses a different word, "which", to distinguish the character.

Refer to the documentation on Keyboard Events for a further treatment of keyboard events.

**DRAFT**
<font size="x-small">This page is not complete.</font>

## Example: Dragging images around

The following example allows moving the image of firefox around the page.

``` html
 <!DOCTYPE html>
 <html>
 <head>
 <style type='text/css'>
 img { position: absolute; }
 </style>

 <script type='text/javascript'>
 window.onload = function() {

   movMeId=document.getElementById("ImgMov");
   movMeId.style.top = "80px";
   movMeId.style.left = "80px";

   document.onmousedown = coordinates;
   document.onmouseup=mouseup;

   function coordinates(e) {
     if (e == null) { e = window.event;}
     var sender = (typeof( window.event ) != "undefined" ) ? e.srcElement : e.target;

     if (sender.id=="ImgMov") {
       mouseover = true;
       pleft = parseInt(movMeId.style.left);
       ptop = parseInt(movMeId.style.top);
       xcoor = e.clientX;
       ycoor = e.clientY;
       document.onmousemove=moveImage;
       return false;
     } else {
         return false;
     }
   }

   function moveImage(e) {
     if (e == null) { e = window.event; }
     movMeId.style.left = pleft+e.clientX-xcoor+"px";
     movMeId.style.top = ptop+e.clientY-ycoor+"px";
     return false;
   }

   function mouseup(e) {
     document.onmousemove = null;
   }
 }
 </script>
 </head>

 <body>
   <img id="ImgMov" src="http://mozcom-cdn.mozilla.net/img/covehead/about/logo/download/logo-only.png" width="64" height="64" />
   <p>Drag and drop around the image in this page.</p>
 </body>

 </html>
```

## Example: Resizing things

<span class="inlineIndicaor todoInline">**FIXME:** *Need Content. Or, remove headline*</span>

## Example: Drawing Lines

<span class="inlineIndicaor todoInline">**FIXME:** *Need Content. Or, remove headline*</span>
