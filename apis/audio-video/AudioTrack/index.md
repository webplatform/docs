{{Page_Title}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|AudioTrack is an object representing an audio portion of a video element.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=Audio tracks are represented on a '''video''' element as an [[apis/audio-video/AudioTrackList|'''AudioTrackList''']] object, which contains one or more audio tracks. The [[apis/audio-video/properties/audioTracks|'''audioTracks''']] property is used to get the '''AudioTrackList''' object, and individual audio tracks are retrieved with indexes into the object.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.10.10

====Properties====
The '''AudioTrack''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[apis/audio-video/properties/enabled{{!}}'''enabled''']]
{{!}}Gets or sets whether an '''AudioTrack''' is enabled.
{{!}}-
{{!}}[[apis/audio-video/properties/id{{!}}'''id''']]
{{!}}Returns the [[apis/audio-video/TextTrackCue{{!}}'''TextTrackCue''']] identifier.
{{!}}-
{{!}}[[apis/audio-video/properties/kind{{!}}'''kind''']]
{{!}}Gets or sets the type or category of the timed text track associated with a '''track''' element.
{{!}}-
{{!}}[[apis/audio-video/properties/label{{!}}'''label''']]
{{!}}Gets or sets the label attribute to give a user a readable title for a text track.
{{!}}-
{{!}}[[apis/audio-video/properties/language{{!}}'''language''']]
{{!}}Gets the BCP47 language tag of an '''AudioTrack''' or [[apis/audio-video/TextTrack{{!}}'''TextTrack''']] if available, or an empty string if not.
{{!}}}

}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/audio-video/AudioTrackList|AudioTrackList]]</code>
*<code>[[apis/audio-video/properties/audioTracks|audioTracks]]</code>
*<code>[[dom/events/DOMContentLoaded|DOMContentLoaded]]</code>
*<code>[[apis/audio-video/events/loadeddata|onloadeddata]]</code>
*<code>video</code>
}}
{{Topics|Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}