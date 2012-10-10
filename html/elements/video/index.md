{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=dom/HTMLVideoElement
|Content=interface HTMLVideoElement : HTMLMediaElement {
           attribute unsigned long width;
           attribute unsigned long height;
  readonly attribute unsigned long videoWidth;
  readonly attribute unsigned long videoHeight;
           attribute DOMString poster;
};
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Beginning with Internet Explorer 9, any audio or video content needs  the correct mime type set on the server, or the files won't play. Internet Explorer 9 supports MP3 audio, and  MP4 audio and video. WebM audio and video files can be supported by installing the WebM components from [http://go.microsoft.com/fwlink/p/?LinkID{{=}}218894 The WebM project]. The following table shows the required settings for your web server to host these files correctly.
{| class="wikitable"
|-
!Media file to serve
!Extension setting
!Mime type setting
|-
|Audio mp3
|mp3
|audio/mpeg
|-
|Audio mp4
|m4a
|audio/mp4
|-
|Audio WebM
|webm
|audio/webm
|-
|Video mp4
|mp4
|video/mp4
|-
|Video webm
|webm
|video/webm
|}
 
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.6


===Members===
The '''video''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''video''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[dom/events/abort|'''onabort''']]
|Fires when the user aborts the download.
|-
|[[apis/audio-video/events/canplay|'''oncanplay''']]
|Occurs when playback is possible, but would require further buffering.
|-
|[[apis/audio-video/events/canplaythrough|'''oncanplaythrough''']]
|Occurs when playback to end is possible without requiring a stop for further buffering.
|-
|[[dom/events/change|'''onchange''']]
|Fires when the contents of the object or selection have changed.
|-
|[[dom/events/drag|'''ondrag''']]
|Fires on the source object continuously during a drag operation.
|-
|[[dom/events/dragend|'''ondragend''']]
|Fires on the source object when the user releases the mouse at the close of a drag operation.
|-
|[[dom/events/dragenter|'''ondragenter''']]
|Fires on the target element when the user drags the object to a valid drop target.
|-
|[[dom/events/dragleave|'''ondragleave''']]
|Fires on the target object when the user moves the mouse out of a valid drop target during a drag operation.
|-
|[[dom/events/dragover|'''ondragover''']]
|Fires on the target element continuously while the user drags the object over a valid drop target.
|-
|[[dom/events/dragstart|'''ondragstart''']]
|Fires on the source object when the user starts to drag a text selection or selected object.
|-
|[[dom/events/drop|'''ondrop''']]
|Fires on the target object when the mouse button is released during a drag-and-drop operation.
|-
|[[apis/audio-video/events/durationchange|'''ondurationchange''']]
|Occurs when the [[apis/audio-video/properties/duration|'''duration''']] attribute is updated.
|-
|[[apis/audio-video/events/emptied|'''onemptied''']]
|Occurs when the media element is reset to its initial state.
|-
|[[apis/audio-video/events/ended|'''onended''']]
|Occurs when the end of playback is reached.
|-
|[[dom/events/error|'''onerror''']]
|Fires when an error occurs during object loading.
|-
|[[dom/events/focus|'''onfocus''']]
|Fires when the object receives focus.
|-
|[[dom/events/focusin|'''onfocusin''']]
|Fires for an element just prior to setting focus on that element.
|-
|[[dom/events/focusout|'''onfocusout''']]
|Fires for the current element with focus immediately after moving focus to another element.
|-
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/keydown|'''onkeydown''']]
|Fires when the user presses a key.
|-
|[[dom/events/keypress|'''onkeypress''']]
|Fires when the user presses an alphanumeric key.
|-
|[[dom/events/keyup|'''onkeyup''']]
|Fires when the user releases a key.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
|-
|[[apis/audio-video/events/loadeddata|'''onloadeddata''']]
|Occurs when media data is loaded at the current playback position.
|-
|[[apis/audio-video/events/loadedmetadata|'''onloadedmetadata''']]
|Occurs when the duration and dimensions of the media have been determined.
|-
|[[apis/audio-video/events/loadstart|'''onloadstart''']]
|Occurs when Internet Explorer begins looking for media data.
|-
|[[dom/events/mousedown|'''onmousedown''']]
|Fires when the user clicks the object with either mouse button.
|-
|[[dom/events/mousemove|'''onmousemove''']]
|Fires when the user moves the mouse over the object.
|-
|[[dom/events/mouseout|'''onmouseout''']]
|Fires when the user moves the mouse pointer outside the boundaries of the object.
|-
|[[dom/events/mouseover|'''onmouseover''']]
|Fires when the user moves the mouse pointer into the object.
|-
|[[dom/events/mouseup|'''onmouseup''']]
|Fires when the user releases a mouse button while the mouse is over the object.
|-
|[[dom/events/mousewheel|'''onmousewheel''']]
|Fires when the wheel button is rotated.
|-
|'''onMSVideoFormatChanged'''
|Occurs when the video format changes.
|-
|'''onMSVideoFrameStepCompleted'''
|Occurs when the video frame has been stepped forward or backward one frame.
|-
|'''onMSVideoOptimalLayoutChanged'''
|Occurs when the '''msIsLayoutOptimalForPlayback''' state changes.
|-
|[[apis/audio-video/events/pause|'''onpause''']]
|Occurs when playback is paused.
|-
|[[apis/audio-video/events/play|'''onplay''']]
|Occurs when the [[apis/audio-video/methods/play|'''play''']] method is requested.
|-
|[[apis/audio-video/events/playing|'''onplaying''']]
|Occurs when the audio or video has started playing.
|-
|[[apis/audio-video/events/progress|'''onprogress''']]
|Occurs to indicate progress while downloading media data.
|-
|[[apis/audio-video/events/ratechange|'''onratechange''']]
|Occurs when the playback rate is increased or decreased.
|-
|[[apis/audio-video/events/ratechange|'''onratechange''']]
|Occurs when the playback rate is increased or decreased.
|-
|[[dom/events/readystatechange|'''onreadystatechange''']]
|Fires when the state of the object has changed.
|-
|[[dom/events/reset|'''onreset''']]
|Fires when the user resets a form.
|-
|[[apis/audio-video/events/seeked|'''onseeked''']]
|Occurs when the seek operation ends.
|-
|[[apis/audio-video/events/seeking|'''onseeking''']]
|Occurs when the current playback position is moved.
|-
|[[dom/events/selectstart|'''onselect''']]
|Fires when the current selection changes.
|-
|[[apis/audio-video/events/stalled|'''onstalled''']]
|Occurs when the download has stopped.
|-
|[[apis/audio-video/events/suspend|'''onsuspend''']]
|Occurs if the load operation has been intentionally halted.
|-
|[[apis/audio-video/events/timeupdate|'''ontimeupdate''']]
|Occurs to indicate the current playback position.
|-
|[[apis/audio-video/events/volumechange|'''onvolumechange''']]
|Occurs when the volume is changed, or playback is muted or unmuted.
|-
|[[apis/audio-video/events/waiting|'''onwaiting''']]
|Occurs when playback stops because the next frame of a video resource is not available.
|}
 

====Methods====
The '''video''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/audio-video/methods/canPlayType|'''canPlayType''']]
|Returns a string that specifies whether the client can play a given media resource type.
|-
|[[dom/methods/compareDocumentPosition|'''compareDocumentPosition''']]
|Compares the position of two nodes in a document.
|-
|[[dom/methods/getAttributeNodeNS|'''getAttributeNodeNS''']]
|Gets an [[dom/attributes|'''attribute''']] object that matches the specified namespace and name.
|-
|[[dom/methods/getAttributeNS|'''getAttributeNS''']]
|Gets the value of the specified attribute within the specified namespace.
|-
|[[dom/methods/getElementsByClassName|'''getElementsByClassName''']]
|Gets a collection of objects that are based on the value of the [[dom/properties/className|'''CLASS''']] attribute.
|-
|[[dom/methods/getElementsByTagNameNS|'''getElementsByTagNameNS''']]
|Gets a collection of objects that are based on the specified element names within a specified namespace.
|-
|[[dom/methods/hasAttributeNS|'''hasAttributeNS''']]
|Determines whether an attribute that has the specified namespace and name exists.
|-
|[[dom/methods/isDefaultNamespace|'''isDefaultNamespace''']]
|Indicates whether or not a namespace is the default namespace for a document.
|-
|[[dom/methods/isEqualNode|'''isEqualNode''']]
|Determines if two nodes are equal.
|-
|[[dom/methods/isSameNode|'''isSameNode''']]
|Determines if two node references refer to the same node.
|-
|[[dom/methods/isSupported|'''isSupported''']]
|Returns a value indicating whether or not the object supports a specific DOM standard.
|-
|[[apis/audio-video/methods/load|'''load''']]
|Resets the '''IHTMLMediaElement''' and loads a new media resource.
|-
|[[dom/methods/lookupNamespaceURI|'''lookupNamespaceURI''']]
|Gets the URI of the namespace associated with a namespace prefix, if any.
|-
|[[dom/methods/lookupPrefix|'''lookupPrefix''']]
|Gets the namespace prefix associated with a URI, if any.
|-
|'''msFrameStep'''
|Steps the video by one frame forward or one frame backward.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|'''msSetVideoRectangle'''
|Sets the dimensions of a sub-rectangle within a video.
|-
|[[apis/audio-video/methods/pause|'''pause''']]
|Pauses the current playback and sets [[apis/audio-video/properties/paused|'''paused''']] to TRUE.
|-
|[[apis/audio-video/methods/play|'''play''']]
|Loads and starts playback of a media resource.
|-
|[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
|Removes the specified attribute from the object.
|-
|[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
|Sets an [[dom/attributes|'''attribute''']] object as part of the object.
|-
|[[dom/methods/setAttributeNS|'''setAttributeNS''']]
|Sets the value of the specified attribute within the specified namespace.
|}
 

====Properties====
The '''video''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/audioTracks|'''audioTracks''']]
|Returns an [[apis/audio-video/AudioTrackList|'''AudioTrackList''']] object with the audio tracks for a given '''video''' element.
|-
|[[apis/audio-video/properties/autobuffer|'''autobuffer''']]
|The [[apis/audio-video/properties/autobuffer|'''autobuffer''']] element is not supported by Internet Explorer 9. Use the [[apis/audio-video/properties/preload|'''preload''']] element instead.

This property is not supported for Metro style apps using JavaScript
|-
|[[apis/audio-video/properties/autoplay|'''autoplay''']]
|Gets or sets a value that indicates whether to start playing the media automatically.
|-
|[[apis/audio-video/properties/buffered|'''buffered''']]
|Gets a collection of buffered time ranges.
|-
|[[apis/audio-video/properties/controls|'''controls''']]
|Gets or sets a flag that indicates whether the client provides a set of controls for the media (in case the developer does not include controls for the player).
|-
|[[apis/audio-video/properties/currentSrc|'''currentSrc''']]
|Gets the address or URL of the current media resource ('''video''','''audio''') that is selected by '''IHTMLMediaElement'''.
|-
|[[apis/audio-video/properties/currentTime|'''currentTime''']]
|Gets or sets the current playback position, in seconds.
|-
|[[apis/audio-video/properties/defaultPlaybackRate|'''defaultPlaybackRate''']]
|Gets or sets the default playback rate when the user is not using fast foward or reverse for a video or audio resource.
|-
|[[apis/audio-video/properties/duration|'''duration''']]
|Gets the duration, in seconds, of the current media resource, a <code>NaN</code> value if duration is not available, or <code>Infinity</code> if the media resource is streaming.
|-
|[[apis/audio-video/properties/ended|'''ended''']]
|Gets information about whether the playback has ended or not.
|-
|[[apis/audio-video/properties/error|'''error''']]
|Gets an '''IHTMLMediaError''' object representing the current error state of the media element.
|-
|[[apis/audio-video/properties/height|'''height''']]
|Gets or sets the height of the video element.
|-
|[[apis/audio-video/properties/initialTime|'''initialTime''']]
|Gets the earliest possible position, in seconds, that the playback can begin.
|-
|[[dom/properties/localName|'''localName''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[apis/audio-video/properties/loop|'''loop''']]
|Gets or sets a flag that specifies whether playback should restart after it completes.
|-
|[[apis/audio-video/properties/muted|'''muted''']]
|Gets or sets a flag that indicates whether the audio (either audio or the audio track on video media) is muted.
|-
|[[dom/properties/namespaceURI|'''namespaceURI''']]
|Retrieves the namespace URI of the fully qualified XML declaration for a node.
|-
|[[apis/audio-video/properties/networkState|'''networkState''']]
|Gets the current network activity for the element.
|-
|[[apis/audio-video/properties/paused|'''paused''']]
|Gets a flag that specifies whether playback is paused.
|-
|[[apis/audio-video/properties/playbackRate|'''playbackRate''']]
|Gets or sets the current speed for the media resource to play. This speed is expressed as a multiple of the normal speed of the media resource.
|-
|[[apis/audio-video/properties/played|'''played''']]
|Gets [[apis/audio-video/HTMLTimeRanges|'''TimeRanges''']] for the current media resource that has been played.
|-
|[[apis/audio-video/properties/poster|'''poster''']]
|Gets or sets a URL of an image to display, for example, like a movie poster. This can be a still frame from the video, or another image if no video data is available.
|-
|[[dom/properties/prefix|'''prefix''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[apis/audio-video/properties/preload|'''preload''']]
|Gets or sets a hint to how much buffering is advisable for a media resource, even if [[apis/audio-video/properties/autoplay|'''autoplay''']] is not specified.
|-
|[[apis/audio-video/properties/seekable|'''seekable''']]
|Returns a [[apis/audio-video/HTMLTimeRanges|'''TimeRanges''']] object that represents the ranges of the current media resource that can be seeked.
|-
|[[apis/audio-video/properties/seeking|'''seeking''']]
|Gets a flag that indicates whether the the client is currently moving to a new playback position in the media resource.
|-
|[[apis/audio-video/properties/src|'''src''']]
|The address or URL of the a media resource ('''video''', '''audio''') that is to be considered.
|-
|[[dom/properties/textContent|'''textContent''']]
|Sets or retrieves the text content of an object and any child objects.
|-
|[[apis/audio-video/properties/videoHeight|'''videoHeight''']]
|Gets the intrinsic height  of a video in CSS pixels, or zero if the dimensions are not known.
|-
|[[apis/audio-video/properties/videoWidth|'''videoWidth''']]
|Gets the intrinsic width of a video in CSS pixels, or zero if the dimensions are not known.
|-
|[[apis/audio-video/properties/volume|'''volume''']]
|Gets or sets the volume level for audio portions of the media element.
|-
|[[apis/audio-video/properties/width|'''width''']]
|Gets or sets the width of the '''video''' element.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
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
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.3
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=1
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=4
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
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
|Safari_mobile_supported=Yes
|Safari_mobile_version=1
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>video object</code>
}}
{{Topics|HTML, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}