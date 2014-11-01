{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, and compat, also better spec link
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
|Description=The following example sets the total duration value when the video is loaded and updates the current playback position as the video plays.
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
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Use the [[dom/HTMLMediaElement/currentTime|'''currentTime''']] property to retrieve the current playback position. For the total length of the audio or video clip, use [[dom/HTMLMediaElement/duration|'''duration''']].
To invoke this event, do one of the following:
*Play the video.
*Move the position indicator on the playback controls.

'''Note'''  This event is fired approximately four times a second.
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
*<code>[[dom/HTMLMediaElement/currentTime|currentTime]]</code>
*<code>[[dom/HTMLMediaElement/duration|duration]]</code>
*<code>[[dom/Element/durationchange|ondurationchange]]</code>
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}