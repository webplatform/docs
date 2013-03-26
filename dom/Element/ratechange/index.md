{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Interface=dom/objects/Event
|Target=dom/Element
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example implements buttons that change the playback rate of a video element (v1) by a factor of 0.2. The '''Resume''' button sets the playback rate back to 1 (100 percent).
|Code=&lt;button onclick{{=}}"document.getElementById('v1').playbackRate +{{=}} 0.2"&gt;Speed Up&lt;/button&gt;
&lt;button onclick{{=}}"document.getElementById('v1').playbackRate -{{=}} 0.2"&gt;Slow Down&lt;/button&gt;
&lt;button onclick{{=}}"document.getElementById('v1').playbackRate {{=}} 1"&gt;Resume&lt;/button&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
This event is raised when the value of [[apis/audio-video/properties/playbackRate|'''playbackRate''']] changes. The playback rate can be increased to a maximum of <code>2</code> (200 percent), or decreased to <code>0</code>.
To invoke this event, do one of the following:
*Increase or decrease the value of [[apis/audio-video/properties/playbackRate|'''playbackRate''']].
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.9.12


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
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
*<code>audio</code>
*<code>audio</code>
*<code>[[dom/document|document]]</code>
*<code>source</code>
*<code>video element</code>
*<code>video element</code>
*<code>video object</code>
*<code>window</code>
*<code>[[apis/audio-video/properties/playbackRate|playbackRate]]</code>
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}