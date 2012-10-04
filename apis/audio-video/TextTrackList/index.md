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
The following example gets the '''TextTrackList''' for the '''video''' element and then displays the [[apis/audio-video/properties/label|'''label''']] for each [[apis/audio-video/TextTrack|'''TextTrack''']].
'''Note'''  To create timed text files in both Web Video Text Track (WebVTT) and Timed Text Markup Language (TTML) formats, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251121 HTML5 Video Caption Maker] on the Windows Internet Explorer test drive site.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Members===
The '''TextTrackList''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''TextTrackList''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/audio-video/methods/item|'''item''']]
|Returns a track from a list that corresponds with the given index based on track order.
|}
 

====Properties====
The '''TextTrackList''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/length|'''length''']]
|Returns the number of tracks in a '''TextTrackList''', [[apis/audio-video/TextTrackCueList|'''TextTrackCueList''']], or [[apis/audio-video/AudioTrackList|'''AudioTrackList''']] list object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/audio-video/TextTrack|TextTrack]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}