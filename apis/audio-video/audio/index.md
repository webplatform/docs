{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/HTMLAudioElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Beginning with Internet Explorer 9, any audio or video content needs  the correct mime type set on the server, or the files won't play. Internet Explorer 9 and  Internet Explorer 10 support MP3 audio, and  MP4 audio and video. WebM audio and video files can be supported by installing the WebM components from [http://go.microsoft.com/fwlink/p/?LinkID{{=}}218894 The WebM project]. The following table shows the required settings for your web server to host these files correctly.
{{{!}} class="wikitable"
{{!}}-
!Media file to serve
!Extension setting
!Mime type setting
{{!}}-
{{!}}Audio mp3
{{!}}mp3
{{!}}audio/mpeg
{{!}}-
{{!}}Audio mp4
{{!}}m4a
{{!}}audio/mp4
{{!}}-
{{!}}Audio WebM
{{!}}webm
{{!}}audio/webm
{{!}}-
{{!}}Video mp4
{{!}}mp4
{{!}}video/mp4
{{!}}-
{{!}}Video webm
{{!}}webm
{{!}}video/webm
{{!}}}
 
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.7


===Members===
The '''audio''' object has these types of members:
*[[#Events{{!}}Events]]
*[[#Methods{{!}}Methods]]
*[[#Properties{{!}}Properties]]


====Events====
The '''audio''' object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[apis/audio-video/events/canplay{{!}}'''oncanplay''']]
{{!}}Occurs when playback is possible, but would require further buffering.
{{!}}-
{{!}}[[apis/audio-video/events/canplaythrough{{!}}'''oncanplaythrough''']]
{{!}}Occurs when playback to end is possible without requiring a stop for further buffering.
{{!}}-
{{!}}[[apis/audio-video/events/durationchange{{!}}'''ondurationchange''']]
{{!}}Occurs when the [[apis/audio-video/properties/duration{{!}}'''duration''']] attribute is updated.
{{!}}-
{{!}}[[apis/audio-video/events/emptied{{!}}'''onemptied''']]
{{!}}Occurs when the media element is reset to its initial state.
{{!}}-
{{!}}[[apis/audio-video/events/ended{{!}}'''onended''']]
{{!}}Occurs when the end of playback is reached.
{{!}}-
{{!}}[[apis/audio-video/events/loadeddata{{!}}'''onloadeddata''']]
{{!}}Occurs when media data is loaded at the current playback position.
{{!}}-
{{!}}[[apis/audio-video/events/loadedmetadata{{!}}'''onloadedmetadata''']]
{{!}}Occurs when the duration and dimensions of the media have been determined.
{{!}}-
{{!}}[[apis/audio-video/events/loadstart{{!}}'''onloadstart''']]
{{!}}Occurs when Internet Explorer begins looking for media data.
{{!}}-
{{!}}[[apis/audio-video/events/pause{{!}}'''onpause''']]
{{!}}Occurs when playback is paused.
{{!}}-
{{!}}[[apis/audio-video/events/play{{!}}'''onplay''']]
{{!}}Occurs when the [[apis/audio-video/methods/play{{!}}'''play''']] method is requested.
{{!}}-
{{!}}[[apis/audio-video/events/playing{{!}}'''onplaying''']]
{{!}}Occurs when the audio or video has started playing.
{{!}}-
{{!}}[[apis/audio-video/events/progress{{!}}'''onprogress''']]
{{!}}Occurs to indicate progress while downloading media data.
{{!}}-
{{!}}[[apis/audio-video/events/ratechange{{!}}'''onratechange''']]
{{!}}Occurs when the playback rate is increased or decreased.
{{!}}-
{{!}}[[apis/audio-video/events/seeked{{!}}'''onseeked''']]
{{!}}Occurs when the seek operation ends.
{{!}}-
{{!}}[[apis/audio-video/events/seeking{{!}}'''onseeking''']]
{{!}}Occurs when the current playback position is moved.
{{!}}-
{{!}}[[apis/audio-video/events/stalled{{!}}'''onstalled''']]
{{!}}Occurs when the download has stopped.
{{!}}-
{{!}}[[apis/audio-video/events/suspend{{!}}'''onsuspend''']]
{{!}}Occurs if the load operation has been intentionally halted.
{{!}}-
{{!}}[[apis/audio-video/events/timeupdate{{!}}'''ontimeupdate''']]
{{!}}Occurs to indicate the current playback position.
{{!}}-
{{!}}[[apis/audio-video/events/volumechange{{!}}'''onvolumechange''']]
{{!}}Occurs when the volume is changed, or playback is muted or unmuted.
{{!}}-
{{!}}[[apis/audio-video/events/waiting{{!}}'''onwaiting''']]
{{!}}Occurs when playback stops because the next frame of a video resource is not available.
{{!}}}
 

====Methods====
The '''audio''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[apis/audio-video/methods/canPlayType{{!}}'''canPlayType''']]
{{!}}Returns a string that specifies whether the client can play a given media resource type.
{{!}}-
{{!}}[[apis/audio-video/methods/load{{!}}'''load''']]
{{!}}Resets the '''IHTMLMediaElement''' and loads a new media resource.
{{!}}-
{{!}}[[apis/audio-video/methods/pause{{!}}'''pause''']]
{{!}}Pauses the current playback and sets [[apis/audio-video/properties/paused{{!}}'''paused''']] to true.
{{!}}-
{{!}}[[apis/audio-video/methods/play{{!}}'''play''']]
{{!}}Loads and starts playback of a media resource.
{{!}}}
 

====Properties====
The '''audio''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[apis/audio-video/properties/autobuffer{{!}}'''autobuffer''']]
{{!}}The [[apis/audio-video/properties/autobuffer{{!}}'''autobuffer''']] element is not supported by Internet Explorer 9. Use the [[apis/audio-video/properties/preload{{!}}'''preload''']] element instead.

This property is not supported for Metro style apps using JavaScript
{{!}}-
{{!}}[[apis/audio-video/properties/autoplay{{!}}'''autoplay''']]
{{!}}Gets or sets a value that indicates whether to start playing the media automatically.
{{!}}-
{{!}}[[apis/audio-video/properties/buffered{{!}}'''buffered''']]
{{!}}Gets a collection of buffered time ranges.
{{!}}-
{{!}}[[apis/audio-video/properties/controls{{!}}'''controls''']]
{{!}}Gets or sets a flag that indicates whether the client provides a set of controls for the media (in case the developer does not include controls for the player).
{{!}}-
{{!}}[[apis/audio-video/properties/currentSrc{{!}}'''currentSrc''']]
{{!}}Gets the address or URL of the current media resource ('''video''','''audio''') that is selected by '''IHTMLMediaElement'''.
{{!}}-
{{!}}[[apis/audio-video/properties/currentTime{{!}}'''currentTime''']]
{{!}}Gets or sets the current playback position, in seconds.
{{!}}-
{{!}}[[apis/audio-video/properties/defaultPlaybackRate{{!}}'''defaultPlaybackRate''']]
{{!}}Gets or sets the default playback rate when the user is not using fast foward or reverse for a video or audio resource.
{{!}}-
{{!}}[[apis/audio-video/properties/duration{{!}}'''duration''']]
{{!}}Gets the duration, in seconds, of the current media resource, a <code>NaN</code> value if duration is not available, or <code>Infinity</code> if the media resource is streaming.
{{!}}-
{{!}}[[apis/audio-video/properties/ended{{!}}'''ended''']]
{{!}}Gets information about whether the playback has ended or not.
{{!}}-
{{!}}[[apis/audio-video/properties/error{{!}}'''error''']]
{{!}}Gets an '''IHTMLMediaError''' object representing the current error state of the media element.
{{!}}-
{{!}}[[apis/audio-video/properties/initialTime{{!}}'''initialTime''']]
{{!}}Gets the earliest possible position, in seconds, that the playback can begin.
{{!}}-
{{!}}[[apis/audio-video/properties/loop{{!}}'''loop''']]
{{!}}Gets or sets a flag that specifies whether playback should restart after it completes.
{{!}}-
{{!}}[[apis/audio-video/properties/muted{{!}}'''muted''']]
{{!}}Gets or sets a flag that indicates whether the audio (either audio or the audio track on video media) is muted.
{{!}}-
{{!}}[[apis/audio-video/properties/networkState{{!}}'''networkState''']]
{{!}}Gets the current network activity for the element.
{{!}}-
{{!}}[[apis/audio-video/properties/paused{{!}}'''paused''']]
{{!}}Gets a flag that specifies whether playback is paused.
{{!}}-
{{!}}[[apis/audio-video/properties/playbackRate{{!}}'''playbackRate''']]
{{!}}Gets or sets the current speed for the media resource to play. This speed is expressed as a multiple of the normal speed of the media resource.
{{!}}-
{{!}}[[apis/audio-video/properties/played{{!}}'''played''']]
{{!}}Gets [[apis/audio-video/HTMLTimeRanges{{!}}'''TimeRanges''']] for the current media resource that has been played.
{{!}}-
{{!}}[[apis/audio-video/properties/preload{{!}}'''preload''']]
{{!}}Gets or sets a hint to how much buffering is advisable for a media resource, even if [[apis/audio-video/properties/autoplay{{!}}'''autoplay''']] is not specified.
{{!}}-
{{!}}[[apis/audio-video/properties/seekable{{!}}'''seekable''']]
{{!}}Returns a [[apis/audio-video/HTMLTimeRanges{{!}}'''TimeRanges''']] object that represents the ranges of the current media resource that can be seeked.
{{!}}-
{{!}}[[apis/audio-video/properties/seeking{{!}}'''seeking''']]
{{!}}Gets a flag that indicates whether the the client is currently moving to a new playback position in the media resource.
{{!}}-
{{!}}[[apis/audio-video/properties/src{{!}}'''src''']]
{{!}}The address or URL of the a media resource ('''video''', '''audio''') that is to be considered.
{{!}}-
{{!}}[[apis/audio-video/properties/volume{{!}}'''volume''']]
{{!}}Gets or sets the volume level for audio portions of the media element.
{{!}}}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=24
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=19
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
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
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Editorial/Deletion_Candidate|MS proprietary}}