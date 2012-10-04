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
Individual cues are returned from a [[apis/audio-video/TextTrackCueList|'''TextTrackCueList''']] object (collection of cues). Cues can also be created and added to a track.
'''Note'''  To create timed text files in both Web Video Text Track (WebVTT) and Timed Text Markup Language (TTML) formats, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251121 HTML5 Video Caption Maker] on the Windows Internet Explorer test drive site.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Members===
The '''TextTrackCue''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''TextTrackCue''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/audio-video/methods/getCueAsHTML|'''getCueAsHTML''']]
|Returns the '''TextTrackCue''' text (caption) as a document fragment consisting of HTML elements and other DOM nodes .
|}
 

====Properties====
The '''TextTrackCue''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/endTime|'''endTime''']]
|Returns the ending time, in seconds, for a text track cue.
|-
|[[apis/audio-video/properties/id|'''id''']]
|Returns the '''TextTrackCue''' identifier.
|-
|[[apis/audio-video/properties/pauseOnExit|'''pauseOnExit''']]
|Returns the pause-on-exit flag on a '''TextTrackCue'''. When the flag is true, playback will pause when it reaches the cue's [[apis/audio-video/properties/endTime|'''endTime''']].
|-
|[[apis/audio-video/properties/startTime|'''startTime''']]
|Returns the text track cue start time in seconds.
|-
|[[apis/audio-video/properties/text|'''text''']]
|Gets '''TextTrackCue''' text in un-parsed form.
|-
|[[apis/audio-video/properties/track (TextTrackCue)|'''track''']]
|Returns the [[apis/audio-video/TextTrack|'''TextTrack''']] object that the '''TextTrackCue''' belongs to, or null otherwise.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}