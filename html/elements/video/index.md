{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs information on codec support. Add more example.
|Checked_Out=No
|Content=Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>video</code> tag allows a developer to embed a video in a document. It is new to HTML5. Different browsers have various format support}}
{{Markup_Element
|DOM_interface=dom/HTMLVideoElement
|Content=== Native video playback without plugins ==
Browsers that support HTML5 video will play the media without the need for external plugins. We no longer need to have Flash installed in order to play video on browsers that support HTML5 video. 

The video formats is made up by a <code>video stream</code> + <code>audio stream.</code>

The three main formats for HTML5 video are: MP4, WebM and OGG Vorbis. 

<pre>
.mp4 = H.264 + AAC
.ogg = Theora + Vorbis
.webm = VP8 + Vorbis
</pre>


== Server MIME Types ==

Addition to declaring multiple encodings, the web server also needs to be instructed on the association between MIME types and co

See [[concepts/internet and web/mime types|MIME types]] to find more information about MIME types and [[tutorials/configuring_mimetypes_on_the_server|Setting up MIME types on your server]] for more information regarding server setup to deliver HTML5 audio and video content. 

== Attributes == 
The attributes (controls, preload, loop) go inside <code><video></code> tag to change the behavior of the embedded video.

== What about old browsers? ==

There are several techniques to ensure that people will be able to access the content we've created. I will cover two of them in this article: Chrome Frame and Flash Fallback


===Chrome Frame===

[[http://www.google.com/chromeframe?prefersystemlevel=true|Chrome Frame]] is a plugin for Internet Explorer (up to version 8) that will allow the older browsers to work with HTML5 content (not just video and audio) as if it supported the features natively. 

===Flash fallback===

You can also use flash as a fallback for when the browser does not support any of the provided formats. Flash supports H264 and Adobe has committed to support the WebM format in their flash player although that time timeline is still not clear. The biggest drawback using Flash as opposed to the Chrome Frame plugin is that you will get the flash player interface instead of  whatever UI you built for your video tag. The details of this technique can be seen in the Quick Guide to Implementing the HTML5 Audio tutorial.

<syntaxhighlight lang="html5" highlight="5-7">
<video width="320" height="240" controls="controls" preload="none">
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  <source src="movie.webm" type="video/webm">
  <object data="movie.mp4" width="320" height="240">
    <embed src="movie.swf" width="320" height="240">
  </object> 
</video>
</syntaxhighlight>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Desired video file should be within src attribute. As a best practice you should also include the controls attribute to show playback and volume controls
|Code=<video src="video.webm" controls="controls"></video>
}}{{Single Example
|Language=HTML
|Description=HTML5 Video Tag can support different encodings
|Code=<video>
            <source src="video.mp4" type="video/mp4" />
            <source src="video.webm" type="video/webm" />
            <source src="video.ogg" type="video/ogg" />
            Your browser does not support the <code>video</code> element. 
            You can download it <a href="video.webm">here</a>.
</video>
|LiveURL=http://code.webplatform.org/gist/5314736
}}
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.6
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/embedded-content.html#the-video-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-video-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=3
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.50
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=MP4 (H.264 + AAC)
|Chrome_supported=Yes
|Chrome_version=3
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Ogg (Theora + Vorbis)
|Chrome_supported=Yes
|Chrome_version=3
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.6
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.50
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=WebM (VP8 + Vorbis)
|Chrome_supported=Yes
|Chrome_version=6
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.60
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.3
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=4
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=MP4 (H.264 + AAC)
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=4.6
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=18.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.5
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Ogg (Theora + Vorbis)
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
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
}}{{Compatibility Table Mobile Row
|Feature=WebM (VP8 + Vorbis)
|Android_supported=Yes
|Android_version=2.3
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
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
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
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Note=Google has announced that [http://blog.chromium.org/2011/01/html-video-codec-support-in-chrome.html H.264 support will be removed from Google Chrome] in the future.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9+
|Note=Beginning with Internet Explorer 9, any audio or video content needs  the correct mime type set on the server, or the files won't play. Internet Explorer 9 supports MP3 audio, and  MP4 audio and video. WebM audio and video files can be supported by installing the WebM components from [http://www.webmproject.org/ The WebM project].
}}{{Compatibility Notes Row
|Browser=Safari
|Note=Safari requires QuickTime to play video.
}}{{Compatibility Notes Row
|Browser=Android
|Version=2.1 - 4.0
|Note=Requires specific handling to run the video element to suport MPEG-4/H.264
}}{{Compatibility Notes Row
|Browser=Firefox
|Note=Last versions of Firefox support MPEG-4/H.264 on Windows Vista, Windows 7, Windows 8, Linux, last versions of Android, and soon everywhere [https://blog.mozilla.org/blog/2013/10/30/video-interoperability-on-the-web-gets-a-boost-from-ciscos-h-264-codec/]
}}
}}
{{See_Also_Section
|Topic_clusters=Video
|External_links=* [[http://diveintohtml5.info/video.html| Video Chapter]] from Dive into HTML5
* [[http://www.elstel.org/html5video/FlashVersusHtml5Video.html.en#ffmpeg Videos for the Web with HTML5 - an Introduction]] convert videos into HTML5 format using ffmpeg or a GUI-frontend
}}
{{Topics|HTML, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}