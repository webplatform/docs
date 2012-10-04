{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The following example gets an '''AudioTrackList''' associated with a '''video''' object and displays the [[apis/audio-video/properties/language|'''language''']] and [[apis/audio-video/properties/enabled|'''enabled''']] status of each [[apis/audio-video/AudioTrack|'''AudioTrack''']] .
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.10.10


===Members===
The '''AudioTrackList''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''AudioTrackList''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/audio-video/events/addtrack|'''onaddtrack''']]
|Occurs when an [[apis/audio-video/AudioTrack|'''AudioTrack''']] is added to the '''AudioTrackList''' on a video object.
|-
|[[apis/audio-video/events/change|'''onchange''']]
|Occurs when an [[apis/audio-video/AudioTrack|'''AudioTrack''']] in the  '''AudioTrackList''' associated with a video is enabled or disabled.
|}
 

====Methods====
The '''AudioTrackList''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/addEventListener|'''addEventListener''']]
|Registers an event handler for the specified event type.
|-
|[[dom/methods/dispatchEvent|'''dispatchEvent''']]
|Sends an event to the current element.
|-
|[[apis/audio-video/methods/getTrackById|'''getTrackById''']]
|Returns the first [[apis/audio-video/AudioTrack|'''AudioTrack''']] with the specified [[apis/audio-video/properties/id|'''id''']]  in an '''AudioTrackList'''.
|-
|[[apis/audio-video/methods/item|'''item''']]
|Returns a track from a list that corresponds with the given index based on track order.
|-
|[[dom/methods/removeEventListener|'''removeEventListener''']]
|Removes an event handler that  the  [[dom/methods/addEventListener|'''addEventListener''']] method registered.
|}
 

====Properties====
The '''AudioTrackList''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/length|'''length''']]
|Returns the number of tracks in a [[apis/audio-video/TextTrackList|'''TextTrackList''']], [[apis/audio-video/TextTrackCueList|'''TextTrackCueList''']], or '''AudioTrackList''' list object.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}