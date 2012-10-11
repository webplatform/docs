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
{{Topics|Events}}
{{Notes_Section
|Notes=
===Remarks===
When the [[apis/audio-video/methods/load|'''load''']] method is called, the media element stops any previously running media and resets the element. Playback restarts immediately if the [[apis/audio-video/properties/autoplay|'''autoplay''']] attribute is specified.
To invoke this event, do the following:
*Call the media element's [[apis/audio-video/methods/load|'''load''']] method.

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
*<code>[[dom/events/abort|onabort]]</code>
*<code>[[apis/audio-video/methods/load|load]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}