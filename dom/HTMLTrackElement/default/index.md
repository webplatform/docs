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
This property defines whether the [[apis/audio-video/TextTrack|'''TextTrack''']] is the default for a given '''video''' element. The presence of the default attribute, regardless of assigned value, in the track element equals true.
If no default is specified, no text track will be displayed with the video. Any track can be selected using the default attribute. If more than one track has the default attribute, the first track with the attribute will be default, and the others will be ignored.
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
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}