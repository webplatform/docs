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
|Description=The following example reads the total duration when the video is loaded and updates the current playback position as the video plays.
|Code=function timeUpdate()
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
}}
}}
{{Notes_Section
|Notes====Remarks===
Use the [[apis/audio-video/properties/duration|'''duration''']] property to determine the new duration of the clip.
This event occurs immediately after [[apis/audio-video/events/loadstart|'''onloadstart''']] and before [[apis/audio-video/events/loadedmetadata|'''onloadedmetadata''']].
To invoke this event, do one of the following:
*Load a media resource.
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
*<code>video object</code>
*<code>window</code>
*<code>Reference</code>
*<code>[[apis/audio-video/events/loadedmetadata|onloadedmetadata]]</code>
*<code>[[apis/audio-video/events/timeupdate|ontimeupdate]]</code>
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}