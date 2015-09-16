---
title: 'video'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'In Progress'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: HTMLMediaElement
    href: /dom/HTMLMediaElement
summary: 'HTML Video element allows creator of a HTML document or view of a Web Application to embed a video for display when a user visits the view or opens HTML document in a web browser.'
tags:
  0: API
  1: Objects
  3: Video
uri: apis/audio-video/video

---
<p><br/></p>
<h2>Summary</h2>
<p>
HTML Video element allows creator of a HTML document or view of a Web Application to embed a video for display when a user visits the view or opens HTML document in a web browser.</p><p>Inherits from <a href="/dom/HTMLMediaElement">HTMLMediaElement</a><a href="/dom/HTMLMediaElement">HTMLMediaElement</a>
</p>
<h2>Properties</h2>
<p><i>No properties.</i>
</p>
<h2>Methods</h2>
<p><i>No methods.</i>
</p>
<h2>Events</h2>
<p><i>No events.</i>
</p>
<h2>Inherited from HTMLMediaElement</h2>
<h3>Properties</h3>

<dl><dt>API Name</dt>
  <dd>Summary</dd>
</dl><dl><dt><a href="/dom/HTMLMediaElement/audioTracks">audioTracks</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/autobuffer">autobuffer</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/autoplay">autoplay</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/buffered">buffered</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/controls">controls</a></dt>
  <dd>Controls attribute used within a Audio element or Video element displays the default media controls defined by the web browser being used to open HTML document or view of a Web Application.</dd>
</dl><dl><dt><a href="/dom/HTMLMediaElement/currentSrc">currentSrc</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/currentTime">currentTime</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/defaultPlaybackRate">defaultPlaybackRate</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/duration">duration</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/ended">ended</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/error">error</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/loop">loop</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/muted">muted</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/networkState">networkState</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/paused">paused</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/playbackRate">playbackRate</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/played">played</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/preload">preload</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/seekable">seekable</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/seeking">seeking</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/src">src</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/textTracks">textTracks</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/volume">volume</a></dt>
  <dd/>
</dl><h3>Methods</h3>

<dl><dt>API Name</dt>
  <dd>Summary</dd>
</dl><dl><dt><a href="/dom/HTMLMediaElement/canPlayType">canPlayType</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/load">load</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/pause">pause</a></dt>
  <dd/>
</dl><dl><dt><a href="/dom/HTMLMediaElement/play">play</a></dt>
  <dd>Loads and starts playback of a media resource.</dd>
</dl><h3>Events</h3>

<dl><dt>API Name</dt>
  <dd>Summary</dd>
</dl><dl><dt><a href="/dom/HTMLMediaElement/canplay">canplay</a></dt>
  <dd>Fires whenever enough data is available to determine whether a media is playable.</dd>
</dl><dl><dt><a href="/dom/HTMLMediaElement/canplaythrough">canplaythrough</a></dt>
  <dd>Fires when enough data is available to determine whether a media is playable at a normal rate without interruptions.</dd>
</dl><dl><dt><a href="/dom/HTMLMediaElement/progress">progress</a></dt>
  <dd>Fires to indicate progress while downloading media data.</dd>
</dl><div class="editors-only">
<p><b>Needs Examples</b>:  This section should include examples. 
</p>
</div>
<h2>Notes</h2>
<h3>Remarks</h3>
<p>Beginning with Internet Explorer 9, any audio or video content needs  the correct mime type set on the server, or the files won't play. Internet Explorer 9 supports MP3 audio, and  MP4 audio and video. WebM audio and video files can be supported by installing the WebM components from <a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?LinkID=218894">The WebM project</a>. The following table shows the required settings for your web server to host these files correctly.
</p>
<table class="wikitable"><tr><th>Media file to serve
</th>
<th>Extension setting
</th>
<th>Mime type setting
</th></tr><tr><td>Audio mp3
</td>
<td>mp3
</td>
<td>audio/mpeg
</td></tr><tr><td>Audio mp4
</td>
<td>m4a
</td>
<td>audio/mp4
</td></tr><tr><td>Audio WebM
</td>
<td>webm
</td>
<td>audio/webm
</td></tr><tr><td>Video mp4
</td>
<td>mp4
</td>
<td>video/mp4
</td></tr><tr><td>Video webm
</td>
<td>webm
</td>
<td>video/webm
</td></tr></table><p> 
</p>
<h3>Standards information</h3>
<ul><li><a rel="nofollow" class="external text" href="http://go.microsoft.com/fwlink/p/?linkid=221374">HTML5 A vocabulary and associated APIs for HTML and XHTML</a>, Section 4.8.6</li></ul><h2>See also</h2>
<h3>Related pages</h3>
<ul><li><code>HTMLVideoElement</code></li></ul>
