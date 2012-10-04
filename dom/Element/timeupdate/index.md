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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example sets the total duration value when the video is loaded and updates the current playback position as the video plays.
|LiveURL=
|Code=
function timeUpdate()
{
    document.getElementById('time').innerHTML {{=}} v1.currentTime;
}
function durationChange()
{
    document.getElementById('duration').innerHTML {{=}} v1.duration;
}
&lt;video id{{=}}"v1" controls{{=}}"true" autoplay{{=}}"1" src{{=}}"video.aac"
    ontimeupdate{{=}}"timeUpdate()" ondurationchange{{=}}"durationChange()"/&gt;
&lt;div&gt;Time: &lt;span id{{=}}"time"&gt;0&lt;/span&gt; of &lt;span id{{=}}"duration"&gt;0&lt;/span&gt; seconds.&lt;/div&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use the [[apis/audio-video/properties/currentTime|'''currentTime''']] property to retrieve the current playback position. For the total length of the audio or video clip, use [[apis/audio-video/properties/duration|'''duration''']].
To invoke this event, do one of the following:
*Play the video.
*Move the position indicator on the playback controls.

'''Note'''  This event is fired approximately four times a second.
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
*<code>[[apis/audio-video/properties/currentTime|currentTime]]</code>
*<code>[[apis/audio-video/properties/duration|duration]]</code>
*<code>[[apis/audio-video/events/durationchange|ondurationchange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}