{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary and compat, also better spec link
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Default_action=
|Content=
|Interface=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=The following example implements buttons that change the [[dom/HTMLMediaElement/volume|'''volume''']] of a video element (v1) by increments of .2 and turn mute on and off. These actions cause the '''onvolumechange''' event to be raised.
|Code=&lt;button onclick{{=}}"document.getElementById('v1').volume +{{=}} 0.2"&gt;Volume Up&lt;/button&gt;
&lt;button onclick{{=}}"document.getElementById('v1').volume -{{=}} 0.2"&gt;Volume Down&lt;/button&gt;
&lt;button onclick{{=}}"document.getElementById('v1').muted {{=}} true;"&gt;Mute&lt;/button&gt;
&lt;button onclick{{=}}"document.getElementById('v1').muted {{=}} false"&gt;Unmute&lt;/button&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The [[dom/HTMLMediaElement/volume|'''volume''']] property of the element represents the current volume level.
The default playback volume is <code>1</code> (100 percent). The playback volume cannot be increased beyond 100 percent.
To invoke this event, do one of the following:
*Increase or decrease the volume.
*Mute or unmute the playback.
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
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/audio-video/audio|audioApi]]</code>
*<code>[[html/elements/audio|audioElement]]</code>
*<code>[[dom/Document|Document]]</code>
*<code>[[html/elements/source|source]]</code>
*<code>[[html/elements/video|videoElement]]</code>
*<code>[[apis/audio-video/video|videoApi]]</code>
*<code>[[dom/Window|Window]]</code>
*<code>Reference</code>
*<code>[[dom/HTMLMediaElement/volume|volume]]</code>
*<code>[[dom/HTMLMediaElement/muted|muted]]</code>
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}