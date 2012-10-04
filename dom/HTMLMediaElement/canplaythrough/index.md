{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Event}}
{{Notes_Section
|Notes=
===Remarks===
The '''oncanplaythrough''' event is raised when data is being fetched at a rate that would allow playback without interruption at the [[apis/audio-video/properties/defaultPlaybackRate|'''defaultPlaybackRate''']]. If the [[apis/audio-video/properties/autoplay|'''autoplay''']] attribute is specified, the video starts playing when '''oncanplaythrough''' is received.
This event occurs after [[apis/audio-video/events/canplay|'''oncanplay''']] and before the first [[apis/audio-video/events/progress|'''onprogress''']] event is received.
To invoke this event, do one of the following:
*Load a media resource.

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.9.12


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>audio</code>
*<code>audio</code>
*<code>[[dom/document|document]]</code>
*<code>source</code>
*<code>video element</code>
*<code>video object</code>
*<code>window</code>
*<code>Reference</code>
*<code>[[apis/audio-video/events/play|onplay]]</code>
*<code>[[apis/audio-video/events/playing|onplaying]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}