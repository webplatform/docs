{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Summary, examples, compatibility, clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLTrackElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The keywords can be one of the following:
*'''subtitles''' - A transcription or translation of the audio dialog.
*'''captions''' - A transcription or translation of the dialog, sound effects, musical cues, or other audio information.
*'''descriptions''' - Textual descriptions of the video component, intended for audio synthesis, such as text-to-speech conversion, when the video component is not viewable by the user.
*'''chapters''' - Chapter titles to be used for navigating the video content.
*'''metadata''' - Information available to be used from script, not displayed in the player or browser.

This property is not implemented for the [[apis/audio-video/AudioTrack|'''AudioTrack''']] object.
'''Note'''  To create timed text files in both Web Video Text Track (WebVTT) and Timed Text Markup Language (TTML) formats, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251121 HTML5 Video Caption Maker] on the Windows Internet Explorer test drive site.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]
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
*<code>track element</code>
*<code>track object</code>
*<code>[[apis/audio-video/TextTrack|TextTrack]]</code>
*<code>[[apis/audio-video/AudioTrack|AudioTrack]]</code>
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}