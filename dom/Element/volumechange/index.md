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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example implements buttons that change the [[apis/audio-video/properties/volume|'''volume''']] of a video element (v1) by increments of .2 and turn mute on and off. These actions cause the '''onvolumechange''' event to be raised.
|LiveURL=
|Code=
&lt;button onclick{{=}}"document.getElementById('v1').volume +{{=}} 0.2"&gt;Volume Up&lt;/button&gt;
&lt;button onclick{{=}}"document.getElementById('v1').volume -{{=}} 0.2"&gt;Volume Down&lt;/button&gt;
&lt;button onclick{{=}}"document.getElementById('v1').muted {{=}} true;"&gt;Mute&lt;/button&gt;
&lt;button onclick{{=}}"document.getElementById('v1').muted {{=}} false"&gt;Unmute&lt;/button&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The [[apis/audio-video/properties/volume|'''volume''']] property of the element represents the current volume level.
The default playback volume is <code>1</code> (100 percent). The playback volume cannot be increased beyond 100 percent.
To invoke this event, do one of the following:
*Increase or decrease the volume.
*Mute or unmute the playback.

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
*<code>[[apis/audio-video/properties/volume|volume]]</code>
*<code>[[apis/audio-video/properties/muted|muted]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}