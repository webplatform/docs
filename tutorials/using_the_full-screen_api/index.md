{{Page_Title|Using the full-screen API}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Dave Gash
|URL=http://docs.webplatform.org/wiki/User:Dgash
|Published=October 12, 2012
}}
{{Summary_Section|An introduction to using the full-screen API.}}
{{Tutorial
|Content===Introduction==
In some browser applications, such as games, and with some elements, such as videos, it is advantageous to present
the content using not just the interior browser window space but the full available screen space, 
without borders or other chrome elements. This might be desired to increase clarity, reduce distraction, 
or improve comprehension of the content.

The full-screen API provides a programmatic method for presenting web content using the user's entire monitor and
lets you direct the browser to make an element&mdash;and its children, if any&mdash;occupy all of the available space.

===Visual comparison===
The screen captures below show a web page containing a video element in normal and full-screen modes.

[[image:fs01-normal.png]]<br/>
''Web page (cropped) with video element in normal mode''

[[image:fs02-full.png]]<br/>
''Web page (reduced) with video element in full-screen mode''

==Use==
Beginning with a web page rendered normally in a standard browser window, the developer can enable elements on the page to
change the display to full-screen. Once in full-screen mode, the mode may be exited either programmatically or
through user interaction.

Two methods control the entry to and exit from full-screen mode, <code>[[dom/methods/requestFullscreen|requestFullscreen()]]</code> and
<code>[[dom/methods/exitFullscreen|exitFullscreen]]()</code>, respectively. The first method is applied to the element, the second to the document object as shown below.

===Entering full-screen mode===
Consider a <code>&lt;video&gt;</code> element as illustrated above. The element we wish to control has an ID
so that it can be addressed programmatically. Also, in this case, the element contains the <code>controls</code>
attribute to allow user control of playback, volume, etc., and two different 
<code>&lt;source&gt;</code> child elements as a fallback against a given browser not recognizing one or the other.

<pre>
<video controls id="myvid">
  <source src="myvideo.webm"></source>
  <source src="myvideo.mp4"></source>
</video>
</pre>

The following script might be used to put the video element into full-screen mode.

<pre>
var elem = document.getElementById("myvid");
elem.requestFullscreen();
</pre>

The video element will now render in full-screen mode, waiting for either a programmatic or user action
to manipulate it or to exit full-screen mode.

===Exiting full-screen mode===
While full-screen mode can be exited via standard user actions such as pressing '''Esc''' or '''F11''',
you can also exit the mode programmatically. For example, the following code creates a button whose onclick
event exits full-screen mode.

<pre>
<input type="button" value="Exit full-screen mode" 
  onclick="document.exitFullscreen()"/>
</pre>

In addition, certain other user actions such as navigating to another web page, changing tabs in a browser,
or switching to another application (e.g., with '''alt-Tab''') will also force an exit from full-screen mode.

===Notification events===
When full-screen mode is successfully entered or exited, the document containing the element receives a
<code>fullscreenchange</code> event. The event itself provides no information about the state of the
mode (i.e., whether it is on or off), but the document's <code>fullscreenElement</code> property can be tested
to determine the mode. A non-null value indicates that full-screen is on, as shown below.

<pre>
if (document.fullscreenElement != null) {
  // full-screen is on
}
else {
  // full-screen is off
}
</pre>

===Failures===
Attempts to enter full-screen mode may not succeed for various reasons. For example, <code>&lt;iframe&gt;</code>s
may have to explicity allow full-screen activity, or certain kinds of content such as windowed plug-ins may 
prevent full-screen activation. In addition, attempting to invoke full-screen mode on a parent or descendant
element of an element that ''does'' allow full-screen mode will fail.

In these cases, the element that requested the full-screen mode will recieve a <code>fullscreenerror</code> event, 
which can be trapped in script and handled appropriately.

==Live example==
To see a live example of this feature, go to
[https://developer.mozilla.org/samples/domref/fullscreen.html this page]. 
Once in the page, play the video and then press '''Enter''' to toggle between full-screen and normal modes.

==Code sample==
In this code sample, based on the live example, a video is presented in a web page. 
As above, the '''Enter''' key allows the user to toggle between full-screen and normal mode.

===Watching for the Enter key===
When the page loads, an event listener is added to detect the '''Enter''' key. 

<pre>
document.addEventListener("keydown", function(e) {
  if (e.keyCode == 13) {
    toggleFullScreen();
  }
}, false);

</pre>

If an '''Enter''' keypress is 
detected, the listener calls a toggle function; if not, it returns <code>false</code> and does nothing.

===Toggling full-screen mode===
When an '''Enter''' keypress is detected, the toggle function either enters full-screen mode if it is
not active or exits full-screen mode if it is active. Prior to entry, a <code>videoElement</code> variable has been
set containing the ID of the video element to be toggled.

<pre>
function toggleFullScreen() {
  if (document.fullscreenElement == null) {
    if (videoElement.requestFullscreen) {
      videoElement.requestFullscreen();
    }
  } else {
    if (document.exitFullscreen) {
      document.exitFullscreen();
    } else
  }
}
</pre>

This function begins by testing the document's <code>fullscreenElement</code> property.

If the <code>fullscreenElement</code> property is null,
then the document ''is not'' in full screen mode. The nested <code>if</code> then determines whether
the element supports the <code>requestFullscreen</code> method and, if so, 
invokes it on the element. If the element does not support the method, the script does nothing.

If the <code>fullscreenElement</code> property is not null,
then the document ''is'' in full screen mode. The nested <code>if</code> then determines whether
the document supports the <code>exitFullscreen</code> method and, if so, 
invokes it on the document. If the document does not support the method, the script does nothing.

==Support==
This API currently has only partial support in modern browsers. 
See the compatibility tables below for the latest information.

==See also==
* [[dom/methods/requestFullscreen]]
* [[dom/methods/exitFullscreen]]
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Full-screen API
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21.0
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=14.0
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=5.1
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Full-screen API
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
{{Topics|Control, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}