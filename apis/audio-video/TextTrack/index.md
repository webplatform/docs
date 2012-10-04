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
The track object contains the collection of [[apis/audio-video/TextTrackCue|'''TextTrackCues''']] (times and text) that are contained in the file that the '''track''' element represents.
You can also get a text track object from the video element through the [[apis/audio-video/properties/textTracks|'''TextTracks''']] property, which returns a [[apis/audio-video/TextTrackList|'''TextTrackList''']] object. The '''TextTrackList''' object contains a collection of '''TextTrack''' objects.
'''Note'''  To create timed text files in both Web Video Text Track (WebVTT) and Timed Text Markup Language (TTML) formats, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251121 HTML5 Video Caption Maker] on the Windows Internet Explorer test drive site.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Members===
The '''TextTrack''' object has these types of members:
*[#events Events]
*[#properties Properties]


====Events====
The '''TextTrack''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/audio-video/events/cuechange|'''oncuechange''']]
|Occurs when a [[apis/audio-video/TextTrackCue|'''TextTrackCue''']] in a '''HTMLTrackElement''' changes.
|}
 

====Properties====
The '''TextTrack''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/activeCues|'''activeCues''']]
|Returns the [[apis/audio-video/TextTrackCue|'''TextTrackCues''']] from the currently active [[apis/audio-video/TextTrackList|'''TextTrackList''']] as a [[apis/audio-video/TextTrackCueList|TextTrackCueList]] object.
|-
|[[apis/audio-video/properties/cues|'''cues''']]
|Returns the list of text track [[apis/audio-video/properties/cues|'''cues''']] as a [[apis/audio-video/TextTrackCueList|'''TextTrackCueList''']] object.
|-
|[[apis/audio-video/properties/kind|'''kind''']]
|Gets or sets the type or category of the timed text track associated with a '''track''' element.
|-
|[[apis/audio-video/properties/label|'''label''']]
|Gets or sets the label attribute to give a user a readable title for a text track.
|-
|[[apis/audio-video/properties/language|'''language''']]
|Gets the BCP47 language tag of an [[apis/audio-video/AudioTrack|'''AudioTrack''']] or '''TextTrack''' if available, or an empty string if not.
|-
|[[apis/audio-video/properties/mode|'''mode''']]
|Sets or gets a value that represents whether a text track is currently disabled, hidden, or showing.
|-
|[[apis/audio-video/properties/readyState|'''readyState''']]
|Returns the readiness state of a '''TextTrack''' with values that let you determine whether the track is loaded, is loading, or failed to load.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}