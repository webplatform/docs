{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <code>track</code> tag specifies text tracks for media elements (audio and video).

This element is used to specify subtitles, caption files or other files containing text, that should be visible when the media is playing.

<code>Track</code> is new to HTML5 and is not yet supported in any major browser.
}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
===Members===
The '''track''' object has these types of members:
*[#events Events]
*[#properties Properties]


====Events====
The '''track''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/audio-video/events/cuechange|'''oncuechange''']]
|Occurs when a [[apis/audio-video/TextTrackCue|'''TextTrackCue''']] in a '''HTMLTrackElement''' changes.
|}
 

====Properties====
The '''track''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/default|'''default''']]
|Gets or sets the default timed text track to use when multiple track elements are specified for a '''video''' element.
|-
|[[apis/audio-video/properties/kind|'''kind''']]
|Gets or sets the type or category of the timed text track associated with a '''track''' element.
|-
|[[apis/audio-video/properties/label|'''label''']]
|Gets or sets the label attribute to give a user a readable title for a text track.
|-
|[[apis/audio-video/properties/src|'''src''']]
|The address or URL of the a media resource ('''video''', '''audio''') that is to be considered.
|-
|[[apis/audio-video/properties/srclang|'''srclang''']]
|Gets or sets the language of the text track data. This attribute is required if "subtitles" is specified in the [[apis/audio-video/properties/kind|'''kind''']] attribute.
|-
|[[apis/audio-video/properties/track (HTMLTrackElement)|'''track''']]
|Returns the [[apis/audio-video/TextTrack|'''TextTrack''']] object that corresponds to a '''track''' element.
|}
 
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
*<code>track object</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}